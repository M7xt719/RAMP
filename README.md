RAMP — Roblox Auto MIDI Player
![Download](https://img.shields.io/github/v/release/M7xt719/RAMP?label=Download&style=for-the-badge&color=6366f1)
![Windows 10 / 11](https://img.shields.io/badge/Windows-10%20%2F%2011%20(64--bit)-0078D6?style=for-the-badge&logo=windows)
![No install needed](https://img.shields.io/badge/Setup-portable%2C%20no%20install-22c55e?style=for-the-badge)
Play MIDI files into any Roblox piano. Auto player with human-like playing,
live MIDI keyboard support, a built-in Synthesia-style visualizer, audio→MIDI
transcription, letter sheets, full theming — one app, no setup.
![Player](pics/player.png)
> Not affiliated with or endorsed by Roblox Corporation.
> Use responsibly and follow the rules of any experience you play in.
---
Download
⬇️ Download the latest RAMP_release.zip
Extract anywhere, run `RAMP.exe` — that's it. Portable: no installer, no
Python, nothing else to download.
Supported:
	
OS	Windows 10 / Windows 11 (64-bit)
Install	None — portable folder, settings live in `%APPDATA%\RAMP`
Internet	Only needed for Cloud transcription, `.mid` links, and updates
Sound out of the box	Yes — pick Microsoft GS Wavetable Synth in Settings → Sound, or load any `.sf2`/`.sfz`
Not supported	macOS / Linux (RAMP sends Windows keystrokes)
RAMP updates itself: when a new version is released here, you'll see
Update available in the logs — Settings → About RAMP → Update & restart
installs it in one click.
> **Windows Defender note:** RAMP sends keystrokes (that's its whole job),
> which some machines flag as a false positive. If the exe vanishes on first
> run: Windows Security → Protection history → Restore, then add the RAMP
> folder as an exclusion. Or build it yourself from this source with
> `build_exe.bat` — then there's nothing to trust but your own build.
---
🎹 Auto player
Plays any `.mid` as Virtual-Piano keypresses — 61-key, 88-key
Transpose, or 88-key Ctrl modes, plus a 128-key extension
Speed control, seeking, playlists with auto-next and loop, sustain pedal
following, per-track muting
Favourites — star your best MIDIs and sort them straight to the top
![Favourites](pics/library-favourites.png)
Global hotkeys — play/pause/stop/speed/panic without leaving Roblox
Overlay mode — clicking RAMP's buttons doesn't steal focus from Roblox,
so the music never stutters while you tweak things mid-song
Smart timing: bounded catch-up keeps the rhythm intact through lag spikes
instead of rubber-banding
🎭 Great Pretender
Human imperfections so it doesn't read as a bot — re-rolled every play.
Warm-up, stage fright, note length drift, offsets, rubato, replayed notes,
even angry spam and wrong notes. Four presets from Subtle to Pro, or
dial in your own.
🏆 MIDI Proof
![MIDI Proof](pics/midi-proof.png)
Show off across the whole keyboard: scales and patterns over any range, up to
Insane difficulty, with octaves and dynamics — proof you're "really
playing".
---
🎼 Visualizer
![Visualizer](pics/visualizer.png)
Falling notes for the auto player, rising notes for live playing — three
sources: Auto Player, Live Keys (every VP keypress on your PC), and
MIDI Connect
Track colors, velocity shading, sustain tails, Rainbow mode, key sound
for live typing
Live FPS/NPS counters, adjustable frame rate (10–2500 fps), S/M/L
keyboard, note travel speed, Focus mode for a clean full-window view
Built for black MIDI: renders 10,000+ notes per second at a locked 60 fps
---
🎤 Audio → MIDI (Transcribe)
![Transcribe](pics/transcribe.png)
Turn an MP3, audio file, or link into a MIDI you can play.
![Models](pics/models.png)
Three models: Kong (fast), Transkun (accurate), Pop2Piano
(cover-style)
Cloud — nothing to install; uploads straight to the service with live
progress and pre-warms the GPU while you're still picking your file
My PC — free and unlimited; one-click model install, CPU or CUDA
Preview your audio before transcribing to make sure it's the right file
Results land in your midi folder with one-click Load in Player
MP3 library sidebar: scan a folder or your whole PC
---
🎛️ Velocity & dynamics
![Velocity](pics/velocity.png)
Auto-volume that follows MIDI dynamics, with full tuning
Dynamics curve — Linear / Soft / Hard / Compressed / Expanded, with
min/max clamps and humanize
Song analysis — analyze a loaded song's dynamics and auto-apply
suggested settings
Full velocity keybind grid (up to all 128 levels), fill/clear tools,
and savable presets
![Velocity keybinds](pics/velocity-keybinds.png)
Auto velocity — shapes dynamics from note density: quiet in calm
passages, swelling through rapid runs (brilliant for flat-velocity MIDIs)
---
🎚️ Octave doubling
![Octave](pics/octave.png)
Thicken the sound by playing every note in up to ×5 octaves at once —
applies live, works on songs and your own live keyboard playing.
---
🔌 Live MIDI keyboard (Connect)
![Connect](pics/connect.png)
Plug in a real MIDI keyboard and RAMP presses the keys in Roblox for you
Two output methods: QWERTY (VP) or MidiConnect numpad protocol
Live velocity, sustain, octave doubling, and the visualizer follows along
---
📜 Qwerty sheets
Turn any MIDI into letter-note sheets with playability levels and automatic
octave shifting.
---
⚙️ Settings & sound
![Settings](pics/settings.png)
Sound output — hear the MIDI as it plays through a built-in SFZ sampler,
any `.sf2` soundfont (FluidSynth), or a MIDI device (VirtualMIDISynth /
OmniMIDI / Microsoft GS Wavetable)
Rebindable hotkeys, focus guard, playback engine options, backup & restore,
system check
🎨 Customize
![Customize](pics/customize.png)
11 quick themes plus full control of every color, font, and UI scale.
---
Building from source
```
1. Install Python 3.13 from python.org (tick "Add to PATH")
2. Run Setup.bat          — installs dependencies
3. Run Start RAMP.bat     — run from source,  or
   Run build_exe.bat      — build your own RAMP.exe
4. Optional: Get_FluidSynth.bat — adds .sf2 soundfont support to your build
```
Credits
Created by M7xt — Dev of Sonata Studios.
Transcription models:
Kong / piano_transcription_inference (ByteDance) ·
Transkun ·
Pop2Piano
Built with PySide6 (Qt) · mido · numpy · pynput · sounddevice · FluidSynth
