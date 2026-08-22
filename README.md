I write things that people will use. C, C++ and Rust are my preferred languages; JavaScript and Python are the ones I use most and know best. Currently in university. 

I'm open to collaboration and contributions.  
Everything below is built and maintained in my free time.

---

## My Best projects

### Relaxy Discord bot

A multipurpose Discord bot running as a sharded fleet with one supervising manager process and N cluster processes. Backend uses MongoDB.

Uses: Node.js v24+, discord.js v14, MongoDB (Mongoose), discord-hybrid-sharding, discord-player (custom fork), node-canvas, ffmpeg, tesseract-ocr.

- 210,000+ users
- 188 commands, 58 event handlers
- ~120,000 lines across 434 source files, with 1,124 commits since September 2021
- Diff-based document storage, multi-process DB workers, local caching
- OCR-backed and perceptual-hash scam detection on posted images
- Cross-server role sync, ban appeals and synced moderation over a credential-less handshake
- Hot reload, rolling restarts andclass patching
- Shard, network and file watchdogs

#### Infrastructure & Ecosystem

The Raspberry Pi runs Void and hosts: the Relaxy! bot, CDN, website, dashboard and health/monitoring services + a few self-correction scripts.  
All services are isolated using **Podman and bubblewrap**. 

https://relaxy.xyz | [Showcase source](https://github.com/MattFor/relaxy-public)

### Relaxy Dashboard

Web dashboard for the bot. Discord OAuth login, three access tiers computed from the OAuth guilds permission bitfield. Has per-user profile customization as well.

Uses: Fastify, custom MongoDB driver, JavaScript, esbuild.

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
- [tracker](https://github.com/MattFor/tracker) (Python) - CLI project tracker with Git repo discovery, search/filtering, bulk editing, configurable output, and a background update daemon.
- [abba](https://github.com/MattFor/abba) (C++26) - Arbitrary Binary Behavioural Anticheat. Memory scanning, file integrity hashing and INI-driven configuration. Still in the early stages.
- [von-neumann-machine-simulator](https://github.com/MattFor/von-neumann-machine-simulator) (Rust, egui/eframe) - Von Neumann architecture simulator with a native GUI.
- [ibus-mozc-system](https://github.com/MattFor/ibus-mozc-system) (Shell, X11) - Scripts and config that make Japanese input under IBus and Mozc work on a keyboard without dedicated JP keys. The entire thing constantly monitors itself to make sure nothing breaks.
- [neural-network](https://github.com/MattFor/neural-network) (C++26) - Multithreaded neural network written from scratch.
- [raytracer](https://github.com/MattFor/raytracer) (C++) - Ray tracer following Ray Tracing in One Weekend.
- [hprint](https://github.com/MattFor/hprint) (C++26) - Header-only utility for centered terminal headers with compile-time border characters and terminal width detection.
- [path-variable-editor](https://github.com/MattFor/path-variable-editor) (Python) - Windows PATH editor that works past the 2047 character limit.

Mirrors of all of my  repositories are also available on [codeberg.org/MattFor](https://codeberg.org/MattFor).

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
