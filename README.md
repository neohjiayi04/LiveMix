## Core Features

### Quick-Trigger Sound Effects
Over 60 built-in sound effects organized into 7 categories:
- **Host/MC** — Welcome, Goodbye, Transition, Countdown, Breaking News, Suspense, Ta-da, Whoosh, Pop, Ding
- **Comedy** — Bruh, Fart, Record Scratch, Crickets, Boing, Slide Whistle, Ba Dum Tss, Fail Horn, Cartoon Run, Evil Laugh
- **Ambient** — Rain, Ocean Waves, Fireplace, Forest Birds, Thunderstorm, Coffee Shop, Wind, River Stream, Night Crickets, Campfire
- **Music** — Lo-fi Beat, Upbeat Funk, Chill Synth, Jazz Piano, Epic Orchestra, Acoustic Guitar, EDM Drop, Hip Hop Beat, Reggae Vibe, Classical Piano
- **Animals** — Dog Bark, Cat Meow, Rooster, Horse Neigh, Duck Quack, Elephant, Lion Roar, Monkey, Crow, Wolf Howl
- **Alerts** — Notification, Message Received, Error Sound, Level Up, Achievement, Coin Collect, Power Up, Game Over, Victory, Alarm
- **Custom** — Your own uploaded sounds

### Import Audio with Precise Control
Import your own audio files (MP3, WAV, OGG, FLAC, M4A, AAC, WebM) and get full control over each one:
- **Start time selection** — Choose exactly which minute and second to begin playback (e.g., skip an intro and start from 1:30)
- **Clickable progress bar** — Visual playback position with seek capability
- **Time display** — Shows current position and total duration
- **Per-audio volume** — Independent volume slider for each imported file
- **Per-audio pitch** — Speed/pitch control (0.5x to 2x)
- **Loop toggle** — Set any audio to repeat continuously
- **Fade In / Fade Out** — Smooth volume transitions for each imported audio
- **Rename** — Double-click to rename any imported audio
- **Add to Board** — Move imported audio to the quick-trigger grid

### Background Music (BGM) with Seamless Looping
8 built-in cinematic background music tracks that loop endlessly without gaps:
- **Mystery Theme** — Minor key, eerie pads, occasional piano notes
- **Investigation Music** — Steady thinking pulse, subtle tension
- **Tavern Ambience** — Warm medieval chords, lute-like arpeggios
- **Horror Atmosphere** — Dissonant drones, heartbeat pulse, creaks
- **Final Battle Music** — Epic fast drums, rising brass
- **Chase Music** — Urgent fast tempo, staccato intensity
- **Peaceful Village** — Gentle melody, soft flute, birdsong
- **Dungeon Crawl** — Dark dripping, echoes, low tension

Each BGM track has:
- Independent volume control
- One-track-at-a-time playback (auto-switches)
- Fade In / Fade Out buttons
- "Now Playing" visual indicator

### Crossfade Transitions
Instead of abrupt audio cuts, SoundBoard Pro crossfades between background tracks:
- Configurable fade duration (2, 3, 4, or 5 seconds)
- When you switch BGM, the current track fades out while the new one fades in simultaneously
- Creates cinematic scene transitions (e.g., fade out "Investigation Music" → fade in "Chase Music")
- Works on imported audio too

### Board Manager
Organize sounds into scenario-specific boards:
- Create named boards (e.g., "D&D Session", "Stream Alerts", "Podcast Intro")
- Switch between boards instantly
- Each board remembers its sound pads
- Saved automatically to browser storage

### Freesound Integration (API Ready)
Search and browse sounds from the Freesound.org library:
- Search by keyword
- Preview results
- Add sounds directly to your board
- Ready to connect with a free Freesound API key

### Master Controls
- **Master volume** — Controls overall output level
- **Pitch shift** — Normal / Low / High pitch for all quick-trigger sounds
- **Stop All** — Instantly silences everything with one click

---

## Technical Details

| Spec | Detail |
|------|--------|
| Platform | Browser-based (Chrome, Firefox, Safari, Edge) |
| Backend | Supabase-ready (auth, database, file storage) |
| Audio Engine | Web Audio API |
| Storage | localStorage (offline) / Supabase (online) |
| File Support | MP3, WAV, OGG, FLAC, M4A, AAC, WebM |
| Cost | Free (self-hosted) or $0/month on Supabase free tier |
| Mobile | Responsive design, works on phones and tablets |

---

## Summary

LiveMix gives you instant sound triggering, imported audio with precise playback control, seamless looping background music, and professional crossfade transitions — all in one lightweight browser tool with zero installation required.
