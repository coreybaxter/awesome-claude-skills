# DS-1 Portfolio Console

A skeuomorphic "portfolio as a hardware device" concept — a single self-contained
`index.html` with zero dependencies, ready to drop onto Netlify as-is.

## The hardware metaphor

Every section is a rack unit bolted into a console:

| Unit | Section | Hardware treatment |
|------|---------|--------------------|
| 01 | Masthead | Brushed-aluminum faceplate, engraved brand plate, working power switch, TUNE knob, VU meter |
| 02 | Nav | Channel-select buttons with per-section LEDs (lit via IntersectionObserver) |
| 03 | About | Green phosphor LCD with boot-up typing effect and scanlines |
| 04 | Work | Projects as swappable modules with mini screens, tags, and status LEDs |
| 05 | Skills | Mixer faders — each skill is a channel level |
| 06 | Contact | Patch bay with 1/4" jack sockets and a TRANSMIT button |

## Interactions

- **POWER switch** — dims the screens/LEDs and re-runs the LCD boot sequence on power-up
- **TUNE knob** — drag it (or focus + arrow keys) to rotate; it retunes the accent hue of every LED, fader, and button on the page
- **VU meter** — needle kicks when you scroll, flutters at idle
- **Nav LEDs** — light up to show which section is on screen

## Accessibility & performance

- Semantic HTML; all controls are real `<button>`/`<a>` elements with focus rings and ARIA
- The knob is a proper `role="slider"` with keyboard support
- `prefers-reduced-motion` disables the typing effect, needle animation, and smooth scroll
- Content stays readable with JS off and with power "off" (the switch is cosmetic only)
- No webfonts, no frameworks, no requests — one file

## Customizing

Search `index.html` for `[REPLACE]` comments: bio copy, project cards
(title/description/tags/link), skill fader levels (`--lvl`), and contact links.
