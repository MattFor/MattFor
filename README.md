I write things that people will use. C, C++ and Rust are my preferred languages; JavaScript and Python are the ones I use most and know best. Currently in university. 

I'm open to collaboration and contributions.  
Everything below is built and maintained in my free time.

---

## My Best projects

### Relaxy! Ecosystem

Everything `relaxy.xyz` related: the bot, the dashboard, the website and the supplementary services. One RaspberryPi (Void) hosts everything isolated under **Podman and bubblewrap**.

https://relaxy.xyz | https://dashboard.relaxy.xyz | https://uptime.relaxy.xyz | https://cdn.relaxy.xyz

#### Relaxy! Bot

A multipurpose Discord bot running as a sharded fleet with one supervising manager process and N cluster processes. Backend uses MongoDB.

Uses: Node.js v24+, discord.js v14, MongoDB (Mongoose), discord-hybrid-sharding, discord-player (custom fork), node-canvas, ffmpeg, tesseract-ocr.

- 210,000+ users
- 188 commands, 58 event handlers
- ~143,000 lines across 436 source files, with 1,129 commits since September 2021
- Diff-based document storage, multi-process DB workers, local caching
- OCR-backed and perceptual-hash scam detection on posted images
- Cross-server role sync, ban appeals and synced moderation over a credential-less handshake
- One shared implementation behind every moderation action, for the usual moderation, dashboard as well as linked servers
- Hot reload, rolling restarts and class patching
- Shard, network and file watchdogs

[Public source](https://github.com/MattFor/relaxy-public-v2) Disclaimer: Half-open source

#### Relaxy! Dashboard

Web dashboard for the bot. Discord OAuth login, three access tiers computed from the OAuth guilds permission bitfield. Has per-user profile customization as well.

Uses: Fastify, the native MongoDB driver, JavaScript, esbuild.

- ~72,000 lines across 62 files
- Discord OAuth-based access control with three permission tiers, per-request authorization checks, per-session CSRF protection and an strict list of modifiable fields

https://dashboard.relaxy.xyz

#### Relaxy! Website

The bot's showcase site, plus the public uptime page. Made it to be as fast as possible

Uses: HTML, CSS, JavaScript.

- 12 pages, ~5,400 lines of JS, ~5,650 lines of CSS
- Changelog, devlog, technical writeup, CDN, Matrix and Minecraft pages
- The uptime page is driven by the health feeds published below

https://relaxy.xyz | https://uptime.relaxy.xyz | [Source](https://github.com/MattFor/relaxy-website)

#### Relaxy! Additions

The scripts and services ensure maximum uptime. Written for runit on Void.

Uses: Node.js, POSIX shell, nftables, runit.

- Probes 23 services on a ten second loop and publishes three JSON feeds (one full, one public, one status)
- Hardware watchdog: pets `/dev/watchdog` and gates it on those health checks. The Pi will reboot automatically on a deadlock
- An uptime ledger with day buckets, incident detection and cause inference, mirrored into a Discord outages channel
- `incident`, a CLI for declaring and annotating an outage by hand
- Keeps sshd at the top of the CPU, IO and OOM priority lists, with a self-contained nftables table putting SSH in band 0 at DSCP CS6 to ensure the Pi stays reachable while it is dying
- error pages generated from the dashboard's own CSS so I don't have to write new ones by hand every time I change something

[Source](https://github.com/MattFor/relaxy-additions)

### emoji-mixer

Node library that generates Google Emoji Kitchen combination image URLs from two emojis.

Uses: JavaScript, webpack (CJS and ESM builds), TypeScript, Python3.

- 122,000+ total downloads ([npm-stat](https://npm-stat.com/charts.html?package=emoji-mixer))
- 1,221 dependent repositories on GitHub
- 619 base emojis, 330,640 valid combinations
- Compatibility data compressed into two lookup tables (codepoints and release dates), so each entry is a two-integer pair instead of a repeated string

https://www.npmjs.com/package/emoji-mixer

### LogEye

Runtime introspection logger for Python. Reports variable assignments, mutations and function calls as they happen, with no debugger and no instrumentation of the target code beyond a decorator.

Uses: Python 3.10+, sys.settrace introspection.

- 9,000+ PyPI downloads
- ~4,700 lines across 12 modules, with 16 test modules and 16 demos
- Educational mode rewrites output into plain sentences for teaching
- Tracks locals, attribute writes, container mutations, arguments and return values

https://pypi.org/project/logeye/

---

## Other projects

- [tracker](https://github.com/MattFor/tracker) (Python) - CLI project tracker with Git repo discovery, search/filtering, bulk editing, configurable output, and a background update daemon.
- [leetcode-zed](https://github.com/MattFor/leetcode-zed) (Rust) - A Zed port of vscode-leetcode. Zed extensions are sandboxed WebAssembly with no tree views or webviews, so this is a native Rust CLI talking to LeetCode's GraphQL and judge endpoints, wrapped in a `wasm32-wasip2` extension that runs it as an MCP server for the Agent Panel.
- [abba](https://github.com/MattFor/abba) (C++26) - Arbitrary Binary Behavioural Anticheat. Memory scanning, file integrity hashing and INI-driven configuration. Still in the early stages.
- [von-neumann-machine-simulator](https://github.com/MattFor/von-neumann-machine-simulator) (Rust, egui/eframe) - Von Neumann architecture simulator with a native GUI, with an easy and a hard mode.
- [ibus-mozc-system](https://github.com/MattFor/ibus-mozc-system) (Python, Shell, X11) - Scripts and config that make Japanese input under IBus and Mozc work on a keyboard without dedicated JP keys. The entire thing constantly monitors itself to make sure nothing breaks.
- [hprint](https://github.com/MattFor/hprint) (C++26) - Header-only utility for centered terminal headers with compile-time border characters and terminal width detection.
- [path-variable-editor](https://github.com/MattFor/path-variable-editor) (Python) - Windows PATH editor that works past the 2047 character limit.
- [download-favourite-discord-gifs](https://github.com/MattFor/download-favourite-discord-gifs) (Python) - Downloads exported Discord favourite GIFs, converts to correct formats with magic byte detection.
- [raytracer](https://github.com/MattFor/raytracer) (C++) - Ray tracer following Ray Tracing in One Weekend.
- [libstrangle-dlsym-fix](https://github.com/MattFor/libstrangle-dlsym-fix) (C) - Fork of milaq's libstrangle with the `__libc_dlsym` lookup error corrected making OpenGL work again on latest glibc.

## Personal
- [g-mang-hud-mattfor-edition](https://github.com/MattFor/g-mang-hud-mattfor-edition) (TF2 HUD) - My modification of a 16+ year old TF2 HUD written in ReScript.
- [.bashrc](https://github.com/MattFor/.bashrc) (Shell) - My .bashrc. System, packaging, media and programming utilities, each documented with what it needs installed.
- [gtk-config](https://github.com/MattFor/gtk-config) (CSS) - My GTK 3 and 4 theme for Void.
- [xfce4-notes-plugin](https://github.com/MattFor/xfce4-notes-plugin) (Vala) - Mirror with the `.git` folder detection removed, along with the folder name in the title.

## Archive

Older projects and university work.

- [neural-network](https://github.com/MattFor/neural-network) (C++26) - Feedforward multithreaded neural network written from scratch, with a test suite. (also submitted as the final project for algorithms & data structures)
- [visual-sorter-v2](https://github.com/MattFor/visual-sorter-v2) (C++20, OpenGL [GLFW], SDL3 and ImGui) - Twelve sorting algorithms drawn one comparison at a time. Performance metrics, graphs and more.
- [emergency-department](https://github.com/MattFor/emergency-department) (C++20, POSIX IPC) - A hospital emergency department where every role is a separate process, coordinating purely through message queues, shared memory, semaphores and signals. Final project for operating systems class.
- [numerical-methods-lab-programs](https://github.com/MattFor/numerical-methods-lab-programs) (C++) - Numerical methods lab programs.
- [dotnet-university](https://github.com/MattFor/dotnet-university) (C#) - Every exercise from the .NET class.
- [relaxy-public-v1](https://github.com/MattFor/relaxy-public-v1) (JavaScript) - The first stripped-down showcase of the bot, from 2023. Superseded by [relaxy-public-v2](https://github.com/MattFor/relaxy-public-v2).
- [grand-archives-discord-bot](https://github.com/MattFor/grand-archives-discord-bot) (JavaScript) - A bot for an old roleplay server. Its `alchemy` command is what [emoji-mixer](https://github.com/MattFor/emoji-mixer) grew out of.
- [escape-the-backrooms-teammaker](https://github.com/MattFor/escape-the-backrooms-teammaker) (C++, Win32) - Team builder used by nightmare runners early in the game's life.
- [matura-exam-preparation](https://github.com/MattFor/matura-exam-preparation) (Python) - Scripts and notes I used as study material for the Matura CS exam.
- [asteroids-old](https://github.com/MattFor/asteroids-old) (C++, SFML), [c-sorting-visualiser](https://github.com/MattFor/c-sorting-visualiser) (C) and [backprop-neural-network-side-project](https://github.com/MattFor/backprop-neural-network-side-project) (Python) - Early things from when I was first learning to program.

Mirrors of my repositories are also available on [codeberg.org/MattFor](https://codeberg.org/MattFor).

---

## Contact

- Discord: mattfor
- Email: mattfor@relaxy.xyz
- Website: https://relaxy.xyz

## Community

I'm a community manager for [Fancy Games](https://store.steampowered.com/publisher/fancy), overseeing [Escape The Backrooms](https://store.steampowered.com/app/1943950/Escape_the_Backrooms/). Join our [Discord server](https://discord.gg/fancygames)!

I also own and run the Escape the Backrooms Community organisation [GitHub](https://github.com/EscapeTheBackroomsCommunity) | [Codeberg](https://codeberg.org/EscapeTheBackrooms).

- [autosplitter](https://github.com/EscapeTheBackroomsCommunity/autosplitter) (ASL) - The LiveSplit autosplitter for the game, covering versions 5.0+. Auto start, splits on level transitions and cutscenes, load removal, and a paused timer in cutscenes, the main menu and on crashes. Based on [uhara](https://github.com/ru-mii/uhara) by ru-mii.
- [UE4SS](https://github.com/EscapeTheBackroomsCommunity/UE4SS) (C++) - Our fork of [RE-UE4SS](https://github.com/UE4SS-RE/RE-UE4SS).
- [community-wiki](https://github.com/EscapeTheBackroomsCommunity/community-wiki) - The community wiki: confirmed features, suggestion guidelines, templates for level, item and entity suggestions, and a guide to running the game on Linux.

The speedrunning bot behind the leaderboards and run verification "The Watcher", originally by [@Reokin](https://github.com/Reokin) is also being rewritten as [etb-speedrun-bot-v2](https://github.com/MattFor/etb-speedrun-bot-v2).

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=mattfor&label=Profile%20views&color=0e75b6&style=flat" alt="Profile Views"/>
</p>
