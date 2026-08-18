I write developer tooling and systems software, things that people will use. C, C++ and Rust are my preferred languages; JavaScript and Python are the ones I use most and know best. Currently in university. 

I'm open to collaboration and contributions.  
Everything below is built and maintained in my own free time.

---

## My Best projects

### Relaxy

A multipurpose Discord bot running as a sharded fleet with one supervising manager process and N cluster processes, backed by MongoDB and running on a Raspberry Pi.

Uses: Node.js, discord.js, MongoDB (Mongoose), discord-hybrid-sharding, discord-player (vendored fork), node-canvas, ffmpeg, tesseract-ocr.

- 210,000+ users
- 188 commands, 58 event handlers
- ~120,000 lines across 434 source files, with 1,124 commits since September 2021
- Diff-based document storage
- OCR-backed and perceptual-hash scam detection on posted images
- Cross-server role sync, ban appeals and synced moderation over a credential-less handshake
- Hot reload and class patching
- Shard and network watchdogs

https://relaxy.xyz | [Showcase source](https://github.com/MattFor/relaxy-public)

### Relaxy Dashboard

Web dashboard for the bot. Discord OAuth login, three access tiers computed from the OAuth guilds permission bitfield. Has per-user profile customization as well.

Uses: Fastify, native MongoDB driver, vanilla JavaScript, esbuild.

- ~43,000 lines across 55 files
- Discord OAuth-based access control with three permission tiers, per-request authorization checks, per-session CSRF protection, and an explicit allow-list of fields that can be modified.

https://dashboard.relaxy.xyz

### emoji-mixer

Node library that generates Google Emoji Kitchen combination image URLs from two emojis.

Uses: JavaScript, webpack (CJS and ESM builds), TypeScript, python3.

- 122,000+ total downloads ([npm-stat](https://npm-stat.com/charts.html?package=emoji-mixer))
- 1,221 dependent repositories on GitHub
- 619 base emojis, 330,640 valid combinations
- Compatibility data compressed into two lookup tables (codepoints and release dates), so each entry is a two-integer pair instead of a repeated string

https://www.npmjs.com/package/emoji-mixer

### LogEye

Runtime introspection logger for Python. Reports variable assignments, mutations and function calls as they happen, with no debugger and no instrumentation of the target code beyond a decorator.

Uses: Python 3.10+, sys.settrace introspection.

- 8,000+ PyPI downloads
- ~3,300 lines across 11 modules, 14 test modules
- Educational mode rewrites output into plain sentences for teaching
- Tracks locals, attribute writes, container mutations, arguments and return values

https://pypi.org/project/logeye/

---

## Other projects

- [relaxy-website](https://github.com/MattFor/relaxy-website) (HTML, CSS, vanilla JS) - Static site with no dependencies and no build step. 12 pages, ~5,400 lines of JS, ~4,500 lines of CSS, plus a separate uptime page.
- [abba](https://codeberg.org/MattFor/abba) (C++) - Arbitrary Binary Behavioural Anticheat. Memory scanning, file integrity hashing and INI-driven configuration. Still in the early stages.
- von-neumann-machine-simulator (Rust, egui/eframe) - Von Neumann architecture simulator with a native GUI. Built with Krisunio, not yet available.
- [ibus-mozc-system](https://github.com/MattFor/ibus-mozc-system) (Shell, X11) - Scripts and config that make Japanese input under IBus and Mozc survive on a keyboard without dedicated JP keys. Health checks verify the input method actually works rather than that its processes exist.
- [neural-network](https://github.com/MattFor/neural-network) (C++) - Multithreaded neural network written from scratch with no ML libraries.
- [raytracer](https://github.com/MattFor/raytracer) (C++) - Ray tracer following Ray Tracing in One Weekend.
- [hprint](https://github.com/MattFor/hprint) (C++) - Header-only utility for centered terminal headers with compile-time border characters and terminal width detection.
- [path-variable-editor](https://github.com/MattFor/path-variable-editor) (Python) - Windows PATH editor that works past the 2047 character limit.

Mirrors of most repositories are also available on [codeberg.org/MattFor](https://codeberg.org/MattFor).

---

## Contact

- Discord: mattfor
- Email: mattfor@relaxy.xyz
- Website: https://relaxy.xyz

## Community

I'm a community manager for [Fancy Games](https://store.steampowered.com/publisher/fancy), overseeing [Escape The Backrooms](https://store.steampowered.com/app/1943950/Escape_the_Backrooms/). Join our [Discord server](https://discord.gg/fancygames)!

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=mattfor&label=Profile%20views&color=0e75b6&style=flat" alt="Profile Views"/>
</p>
