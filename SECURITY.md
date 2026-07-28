# Security & Antivirus False Positives

RAMP is open-source and does not contain malware. This document explains the
antivirus situation honestly, tells you how to verify RAMP for yourself, and —
if you maintain a fork or a mirror — how to clear the false-positive warnings
properly (not by hiding anything, which doesn't work and shouldn't).

---

## The short version

- RAMP **does not** access your browser, cookies, Roblox login, or passwords.
  There is no such code in this repository. Search it: `cookie`, `chrome`,
  `login`, `credential` — none of them touch browser or account data.
- Some antivirus tools flag it anyway. That is a **false positive** caused by
  *how* RAMP is packaged and *what legitimate feature* it has (sending keys),
  not by anything it actually does to your data.
- The correct fixes are **code-signing** and **submitting the false positive to
  vendors**, both covered below. Trying to "hide" the warnings is what real
  malware does, it does not actually work on modern Windows, and RAMP will
  never do it.

---

## Exactly what RAMP accesses (audited)

**Network** — RAMP only ever contacts:

| Endpoint | When | Why |
|---|---|---|
| `api.github.com/repos/M7xt719/RAMP/releases/latest` | On launch | Check for a new RAMP version |
| `github.com/.../RAMP` release asset | Only if you accept an update | Download the new build |
| Transcription service (`*.modal.run`) | Only when you press **Transcribe** | Turn your chosen audio into MIDI |
| Transkun / FluidSynth / soundfont hosts | Only if you enable those optional features | One-time model/soundfont download |

That is the complete list. RAMP makes **no other network calls**. It does not
"phone home", send telemetry, or upload anything on its own.

**Files** — RAMP reads/writes:

- `%APPDATA%\RAMP\` — its settings, logs, and reference data.
- Its own `midi\` folder — songs and transcription output.
- Folders **you explicitly point it at** (your Music/Downloads) — only to list
  songs to play. It does not scan your drive.

**Input** — RAMP **sends** key presses to the focused window to play piano. It
does **not** record or log what you type. (The optional "note logging" feature
logs which *piano notes RAMP itself played*, to its own log file, for
debugging — never your keystrokes.)

---

## Why antivirus flags it (the real reasons)

1. **PyInstaller packaging.** RAMP is Python bundled into one `.exe`. AV engines
   flag PyInstaller binaries very aggressively because some malware uses the
   same packer. This is the #1 cause and it is pure guilt-by-association.
2. **It sends keystrokes.** An auto-player *must* send keys (`SendInput`). That
   is the same API a keylogger could use, so behavioural scanners flag it. RAMP
   only sends; it never captures.
3. **Unsigned + low reputation.** No paid code-signing certificate yet, and a
   small download count, so Windows SmartScreen has no reputation record and
   warns by default on anything new and unsigned.

None of these are "RAMP does something bad." They are "RAMP looks, to a dumb
heuristic, like the *category* of thing that could." That is what a false
positive is.

---

## Verify RAMP yourself (recommended)

1. **Read the code.** Nothing here is obfuscated or encrypted. The keystroke
   sending is in `engine/sendinput_block.py` and `ramp_player.py`; the only
   network code is the update check and the transcription upload.
2. **Watch its network.** Open Windows **Resource Monitor → Network**, run RAMP,
   and confirm it only talks to GitHub (until you press Transcribe).
3. **Build it yourself.** Run `build_exe.bat` to produce your own `RAMP.exe`
   from this exact source. Then you have proof of what's inside.
4. **Scan on VirusTotal** and look at *which* engines flag it — you'll see it's
   mostly heuristic/generic detections (names like `Wacatac`, `Convagent`,
   `AIDetect`, `ML.Attribute`), which are the classic false-positive signatures
   for packed Python apps, not real named malware families.

---

## Clearing the warnings — the legitimate ways

### 1. Submit the false positive to Microsoft (free, fixes it for everyone)

Microsoft has a form to report a file that Defender wrongly flags. Once they
review and clear it, Defender stops flagging that build for **all** users:

- Go to Microsoft's **"Submit a file for malware analysis"** page
  (search: *Microsoft Security Intelligence submit a file*).
- Choose **"Incorrectly detected as malware / PUA"**.
- Upload the exact `RAMP.exe` from the release, and in the notes explain:
  *"Open-source Roblox auto-piano-player. PyInstaller-packed Python. Uses
  SendInput to send key presses (its core feature). No network activity except
  a GitHub update check. Source: <repo link>. This is a heuristic false
  positive."*

Do the same at the other big vendors if users report them (Avast/AVG,
Bitdefender, Kaspersky, Norton, McAfee all have false-positive forms).

### 2. Code-sign the executable (the real long-term fix)

Signing is what actually removes SmartScreen warnings for good:

- **OV (Organization Validation) certificate** — ~£150–250/yr (Sectigo,
  DigiCert, SSL.com). Warnings drop off as the signed app builds reputation.
- **EV (Extended Validation) certificate** — ~£250–400/yr. Removes SmartScreen
  warnings **immediately**, no reputation wait, because EV certs carry instant
  trust. This is the fastest fix if the budget allows.
- Sign with Microsoft's `signtool` after building:
  `signtool sign /fd SHA256 /tr <timestamp-url> /td SHA256 /a RAMP.exe`

Until then, publishing SHA-256 hashes of each release (below) lets people
confirm their download matches the official build.

### 3. Publish hashes so downloads are verifiable

Each release should list the SHA-256 of `RAMP.exe` so anyone can check their
copy wasn't tampered with:

```powershell
Get-FileHash .\RAMP.exe -Algorithm SHA256
```

---

## Reporting a real concern

If you find something in RAMP that genuinely worries you — not a heuristic AV
flag, but actual code — open an issue or contact the maintainer directly.
Point to the specific file and lines and it'll be explained or fixed.

**Only download RAMP from the official Releases page of this repository.** A
build hosted anywhere else is not guaranteed to be RAMP and could have been
modified by someone else.
