fix(audio): resolve silent playback for generated sound effects and BGM

- Await AudioContext.resume() before scheduling playback to avoid
  scheduling sources on a still-suspended context
- Remove dead duplicate playSound/resumeCtx stub
- Commit procedurally generated buffer data via copyToChannel(),
  since writes to getChannelData()'s returned array aren't reliably
  linked back to the AudioBuffer on all browsers
- Imported/uploaded audio was unaffected (decodeAudioData fills
  buffers internally), which was the key diagnostic clue

Fix Explanation
Bug 1 — AudioContext resume race condition

Cause: resumeCtx() called audioCtx.resume() without awaiting it, so source.start() could be scheduled while the context was still suspended, causing silent/inconsistent playback (especially on the very first interaction).
Fix: resumeCtx() now returns the resume promise; all playback entry points (playSound, playBGM, fadeInBGM, toggleImportedPlay, fadeInImported) are async and await resumeCtx() before scheduling audio. Also removed a leftover dead/broken duplicate playSound/resumeCtx stub.

Bug 2 — Procedurally generated audio (sound effects & BGM) silent; imported files fine

Cause: Every generator wrote sample data directly into the array returned by AudioBuffer.getChannelData(0). On some browser engines that array isn't guaranteed to be a live reference back into the buffer, so the generated waveform never actually reached the buffer that gets played. Imported/uploaded audio was unaffected because decodeAudioData() fills its buffer internally, bypassing this path entirely.
Fix: Added b.copyToChannel(c,0) immediately before returning (or storing) every generated buffer — across all 70 sound-effect generators, all 8 BGM track generators, and the mock Freesound generator — which explicitly and reliably commits the written data into the real AudioBuffer on every browser.