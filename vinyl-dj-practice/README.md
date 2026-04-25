# Vinyl DJ Practice

A browser-based sandbox for practicing the **manual** parts of vinyl mixing — pitch faders, nudging, cue points, and beatmatching by ear — without needing a turntable, mixer, or even a real audio file.

Built for techno/house bedroom practice. Just open `index.html` in any modern browser. No build step, no install.

## What it gives you

- **Two decks** with realistic transport: Play, Cue (hold to preview from cue point, release to return), Set Cue, Restart.
- **Pitch fader** with selectable range (±8 / ±16 / ±50%), exactly like a Technics-style turntable.
- **Nudge** buttons that temporarily speed up / slow down the deck — your stand-in for touching the platter or the record edge.
- **Per-deck 3-band EQ** and volume.
- **Crossfader** with equal-power curve, master, and headphone level.
- **Split-cue routing**: cue feeds the left channel, master feeds the right, so you can practice with regular headphones the way DJs do live.
- **Three practice modes**:
  - **Easy** — BPM, waveforms, and a phase meter visible. Good for getting started.
  - **Medium** — BPM hidden, waveforms hidden, phase meter visible.
  - **Vinyl** — all visuals off. You use your ears. There is a `Reveal BPM` button if you want to confirm after attempting.
- **Built-in synthesized loops**: techno @ 128, house @ 124, tech-house @ 126.4 — for instant practice without uploading anything. Mix them against each other or against your own files.
- **File upload**: drop in any audio your browser can decode (MP3 / WAV / FLAC / M4A on most browsers). BPM is auto-detected.
- **Tap tempo** if auto-detect is off.

## How to practice

1. Pick **Vinyl** mode at the top. (You can drop down to Easy if it's too hard at first.)
2. Load Deck A — either a built-in loop or your own track. Hit **Play**.
3. Load Deck B with another track at a similar tempo.
4. Plug in headphones. Hold **CUE** on Deck B to preview it; you'll hear Deck B in your **left** ear and the master (Deck A) in your **right** ear.
5. While holding CUE, drag Deck B's **pitch fader** until the kicks sound like they're at the same tempo.
6. Tap **Nudge +** / **Nudge −** to push Deck B's beat into phase with Deck A. Short nudges, listen, repeat.
7. When the beats lock, release CUE on a downbeat (so Deck B re-cues) and time **Play** to a downbeat in Deck A — the way you'd drop a needle.
8. Slide the crossfader. Keep nudging to hold phase as the records drift apart.
9. Toggle on **Show phase meter** while learning — green dot = locked, drifting away from center means you're losing it.

## Keyboard shortcuts

- `Q` / `P` — Play/Pause Deck A / B
- `A` / `L` — Hold to CUE Deck A / B (release to return to cue point)
- `Z` / `X` — Nudge Deck A down / up (hold)
- `,` / `.` — Nudge Deck B down / up (hold)

## Notes / caveats

- BPM detection is rough — it works best on 4-on-the-floor music with a clear kick. If it's wrong, hit **Tap tempo** four times.
- The platter graphic is purely visual; you can't drag it like a jog wheel. Nudge buttons replace that.
- This is a single static HTML file. Open it directly (`file://`) or serve it with `python3 -m http.server`.
