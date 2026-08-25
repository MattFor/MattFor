<div align="center">

[![Website](https://img.shields.io/badge/mattfor.com-cc056b?style=flat-square&logo=firefoxbrowser&logoColor=white)](https://mattfor.com)
[![Email](https://img.shields.io/badge/mattfor%40relaxy.xyz-a02074?style=flat-square&logo=maildotru&logoColor=white)](mailto:mattfor@relaxy.xyz)
[![Codeberg](https://img.shields.io/badge/codeberg-733b7d?style=flat-square&logo=codeberg&logoColor=white)](https://codeberg.org/MattFor)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-support-465686?style=flat-square&logo=kofi&logoColor=white)](https://ko-fi.com/relaxy)
[![Profile views](https://komarev.com/ghpvc/?username=mattfor&label=Profile%20views&color=1a718f&style=flat-square)](https://github.com/MattFor)

</div>

I write things that people use.  
C, C++ and Rust are my preferred languages; JavaScript and Python are the ones I use most and know best. Currently
studying in university.

I'm open to collaboration and contributions.  
Everything below is built and maintained in my free time.

---

## My Best projects

### Relaxy! Ecosystem<a href="https://github.com/MattFor/relaxy-public-v2"><img align="right" src="https://img.shields.io/badge/lines%20of%20code-~250k-0e75b6?style=flat-square" alt="lines of code"></a><a href="https://uptime.relaxy.xyz"><img align="right" hspace="1" src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Frelaxy.xyz%2Fstatus.json&query=%24.bot.totalUsers&label=users&style=flat-square&color=2ea043" alt="users"></a><img align="right" hspace="1" src="https://img.shields.io/badge/-6e7681?style=flat" alt=""><a href="https://cdn.relaxy.xyz"><img align="right" hspace="1" src="https://img.shields.io/badge/cdn-0e75b6?style=flat-square" alt="cdn"></a><a href="https://uptime.relaxy.xyz"><img align="right" hspace="1" src="https://img.shields.io/badge/uptime-0e75b6?style=flat-square" alt="uptime"></a><a href="https://dashboard.relaxy.xyz"><img align="right" hspace="1" src="https://img.shields.io/badge/dashboard-0e75b6?style=flat-square" alt="dashboard"></a><a href="https://relaxy.xyz"><img align="right" hspace="1" src="https://img.shields.io/badge/relaxy.xyz-0e75b6?style=flat-square" alt="relaxy.xyz"></a>

Everything `relaxy.xyz` related: the bot, the dashboard, the website and the supplementary services.  
A single RaspberryPi hosts everything isolated under Podman and bubblewrap.
<!--  <a href="https://voidlinux.org/"><img src="https://img.shields.io/badge/-478061?style=flat-square&logo=voidlinux&logoColor=white" height="15" style="vertical-align: 0px;"></a> -->

<table width="100%">
<tr>
<td valign="top">
<details>
<summary><b>Discord&nbsp;Bot</b></summary>

A multipurpose Discord bot running as a sharded fleet with one supervising manager process and N cluster processes.
Backend uses MongoDB.

Uses: Node.js v24+, discord.js v14, MongoDB (Mongoose), discord-hybrid-sharding, discord-player (custom fork),
node-canvas, ffmpeg, tesseract-ocr.

- 210,000+ users
- 188 commands, 58 event handlers
- Diff-based document storage, multi-process DB workers, local caching
- OCR-backed and perceptual-hash scam detection on posted images
- Cross-server role sync, ban appeals and synced moderation over a credential-less handshake
- One shared implementation behind every moderation action, for the usual moderation, dashboard as well as linked
  servers
- Hot reload, rolling restarts and class patching
- Shard, network and file watchdogs

[![source](https://img.shields.io/badge/public%20source-half--open-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/relaxy-public-v2)

</details>
</td>
<td valign="top">
<details>
<summary><b>Dashboard</b></summary>

Web dashboard for the bot. Discord OAuth login, three access tiers computed from the OAuth guilds permission bitfield.
Has per-user profile customization as well.

Uses: Fastify, the native MongoDB driver, JavaScript, esbuild.

- Discord OAuth-based access control with three permission tiers, per-request authorization checks, per-session CSRF
  protection and a strict list of modifiable fields

</details>
</td>
<td valign="top">
<details>
<summary><b>Website</b></summary>

The bot's showcase site, plus the public uptime page. I've designed it from the ground up to be as fast as possible.

Uses: HTML, CSS, JavaScript.

- 12 pages, ~5,400 lines of JS, ~5,650 lines of CSS
- Changelog, devlog, technical writeup, CDN, Matrix and Minecraft pages
- The uptime page is driven by the health feeds published below

[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/relaxy-website)

</details>
</td>
<td valign="top">
<details>
<summary><b>Additions</b></summary>

The scripts and services that ensure maximum possible uptime. Written for runit on Void.

Uses: Node.js, POSIX shell scripts, nftables, runit.

- Probes 24 services on a ten-second loop and publishes three JSON feeds (one full, one public, one status)
- Hardware watchdog that pets `/dev/watchdog`; makes the Pi will reboot automatically on a deadlock
- An uptime ledger with day buckets, incident detection and cause inference, mirrored into a Discord outages channel
- `incident` CLI tool for declaring and annotating outages
- Scripts to keep sshd at the top of the CPU, IO and OOM priority lists, with a self-contained nftables table putting
  SSH in band 0 at DSCP CS6 to ensure the Pi stays reachable while it is dying
- error pages generated from the dashboard's own CSS, so I don't have to write new ones by hand every time I change
  something

[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/relaxy-additions)

</details>
</td>
</tr>
</table>

### emoji-mixer<a href="https://github.com/MattFor/emoji-mixer"><img align="right" hspace="1" src="https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white" alt="source"></a><a href="https://www.npmjs.com/package/emoji-mixer"><img align="right" hspace="1" src="https://img.shields.io/npm/v/emoji-mixer?style=flat-square&color=cb3837&logo=npm&logoColor=white" alt="npm"></a>

Node library that generates Google Emoji Kitchen combination image URLs from two emojis.

Uses: JavaScript, webpack (CJS and ESM builds), TypeScript, Python3.

- 122,000+ total downloads ([npm-stat](https://npm-stat.com/charts.html?package=emoji-mixer))
- 1,221 dependent repositories on GitHub
- 619 base emojis, 330,640 valid combinations
- Compact compatibility data is 2.4 MB, down from the 96 MB original.

### LogEye<a href="https://github.com/MattFor/logeye"><img align="right" hspace="1" src="https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white" alt="source"></a><a href="https://pypi.org/project/logeye/"><img align="right" hspace="1" src="https://img.shields.io/pypi/pyversions/logeye?style=flat-square&color=0e75b6" alt="Python"></a><a href="https://pypi.org/project/logeye/"><img align="right" hspace="1" src="https://img.shields.io/pypi/v/logeye?style=flat-square&color=3775A9&logo=pypi&logoColor=white" alt="PyPI"></a>

Runtime introspection logger for Python. Reports variable assignments, mutations and function calls as they happen, with
no debugger and no instrumentation of the target code beyond a decorator.

Uses: Python 3.10+, sys.settrace introspection.

- 9,000+ PyPI downloads
- ~4,700 lines across 12 modules, with 16 test modules and 16 demos
- Educational mode rewrites output into plain sentences for teaching
- Tracks locals, attribute writes, container mutations, arguments and return values

### simple-project-tracker<a href="https://github.com/MattFor/simple-project-tracker"><img align="right" hspace="1" src="https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white" alt="source"></a><a href="https://github.com/MattFor/simple-project-tracker/actions/workflows/ci.yml"><img align="right" hspace="1" src="https://img.shields.io/github/actions/workflow/status/MattFor/simple-project-tracker/ci.yml?style=flat-square&label=CI&logo=githubactions&logoColor=white" alt="CI"></a><a href="https://github.com/MattFor/simple-project-tracker/blob/main/LICENSE"><img align="right" hspace="1" src="https://img.shields.io/badge/license-MIT-0e75b6?style=flat-square" alt="License"></a><a href="https://github.com/MattFor/simple-project-tracker"><img align="right" hspace="1" src="https://img.shields.io/badge/python-3.11%2B-3775A9?style=flat-square&logo=python&logoColor=white" alt="Python"></a>

CLI project tracker with Git repo discovery, search/filtering, bulk editing, configurable output, and a background
update daemon.

Uses: Python 3.11+.

- ~10,500 lines across 35 modules, with 17 test modules on top
- 15 commands, each with aliases and a fused short version
- Frecency-based name resolution
- Undoable edits, a background daemon, shell completion for bash, zsh and fish, and a `man` page

---

## Other projects

- [leetcode-zed](https://github.com/MattFor/leetcode-zed) (Rust) - A Zed port of vscode-leetcode. Zed extensions are
  sandboxed WebAssembly with no tree views or webviews (SAD!) so this is a native Rust CLI talking to LeetCode's GraphQL
  and judge endpoints, wrapped in a `wasm32-wasip2` extension that runs it as an MCP server for the Agent Panel.
- [abba](https://github.com/MattFor/abba) (C++26) - Arbitrary Binary Behavioural Anticheat. Memory scanning, file
  integrity hashing and INI-driven configuration. Still work in progress!
- [von-neumann-machine-simulator](https://github.com/MattFor/von-neumann-machine-simulator) (Rust, egui/eframe) - Von
  Neumann architecture simulator with a native GUI.
- [ibus-mozc-system](https://github.com/MattFor/ibus-mozc-system) (Python, Shell, X11) - Scripts and config that make
  Japanese input under IBus and Mozc work on a keyboard without dedicated JP keys.
- [xfce-tiler](https://github.com/MattFor/xfce-tiler) (Python, X11) - Quadrant, half and directional window tiling for
  XFCE and xfwm4.
- [hprint](https://github.com/MattFor/hprint) (C++26) - Header-only utility for centered terminal headers with
  compile-time border characters and terminal width detection.
- [path-variable-editor](https://github.com/MattFor/path-variable-editor) (Python) - Windows PATH editor that works past
  the 2047 character limit.
- [download-favourite-discord-gifs](https://github.com/MattFor/download-favourite-discord-gifs) (Python) - Downloads
  exported Discord favourite GIFs, converts to correct formats with magic byte detection.
- [raytracer](https://github.com/MattFor/raytracer) (C++) - Ray tracer following Ray Tracing in One Weekend.
- [libstrangle-dlsym-fix](https://github.com/MattFor/libstrangle-dlsym-fix) (C) - Fork of milaq's libstrangle with the
  `__libc_dlsym` lookup error corrected making OpenGL work again on latest glibc.

<details>
<summary><b>Personal</b> - Random configs and themes that I use</summary>

- [g-mang-hud-mattfor-edition](https://github.com/MattFor/g-mang-hud-mattfor-edition) (TF2 HUD) - My modification of a
  16+ year old TF2 HUD written in ReScript.
- [.bashrc](https://github.com/MattFor/.bashrc) (Shell) - My .bashrc. System, packaging, media and programming
  utilities, each documented with what it needs installed.
- [gtk-config](https://github.com/MattFor/gtk-config) (CSS) - My GTK 3 and 4 theme for Void.
- [xfce4-notes-plugin](https://github.com/MattFor/xfce4-notes-plugin) (Vala) - Mirror with the `.git` folder detection
  removed, along with the folder name in the title.

</details>

<details>
<summary><b>Archive</b> - University work and older projects</summary>

#### University

- [neural-network](https://github.com/MattFor/neural-network) (C++26) - Feedforward multithreaded neural network written
  from scratch, with a test suite. (also submitted as the final project for algorithms & data structures)
- [visual-sorter-v2](https://github.com/MattFor/visual-sorter-v2) (C++20, OpenGL [GLFW], SDL3 and ImGui) - Twelve
  sorting algorithms drawn one comparison at a time. Performance metrics, graphs and more.
- [emergency-department](https://github.com/MattFor/emergency-department) (C++20, POSIX IPC) - A hospital emergency
  department where every role is a separate process, coordinating purely through message queues, shared memory,
  semaphores and signals. Final project for operating systems class.
- [numerical-methods-lab-programs](https://github.com/MattFor/numerical-methods-lab-programs) (C++) - Numerical methods
  lab programs.
- [dotnet-university](https://github.com/MattFor/dotnet-university) (C#) - Every exercise from the .NET class.

#### Older projects

- [relaxy-public-v1](https://github.com/MattFor/relaxy-public-v1) (JavaScript) - The first stripped-down showcase of the
  bot, from 2023. Superseded by [relaxy-public-v2](https://github.com/MattFor/relaxy-public-v2).
- [grand-archives-discord-bot](https://github.com/MattFor/grand-archives-discord-bot) (JavaScript) - A bot for an old
  roleplay server. Its `alchemy` command is what [emoji-mixer](https://github.com/MattFor/emoji-mixer) grew out of.
- [escape-the-backrooms-teammaker](https://github.com/MattFor/escape-the-backrooms-teammaker) (C++, Win32) - Team
  builder used by nightmare runners early in the game's life.
- [matura-exam-preparation](https://github.com/MattFor/matura-exam-preparation) (Python) - Scripts and notes I used as
  study material for the Matura CS exam.
- [asteroids-old](https://github.com/MattFor/asteroids-old) (C++,
  SFML), [c-sorting-visualiser](https://github.com/MattFor/c-sorting-visualiser) (C)
  and [backprop-neural-network-side-project](https://github.com/MattFor/backprop-neural-network-side-project) (Python) -
  Early things from when I was first learning to program.

</details>

Mirrors of my repositories are also available on [codeberg.org/MattFor](https://codeberg.org/MattFor).

---

## Contact

- Discord: mattfor
- Email: mattfor@relaxy.xyz
- Website: https://mattfor.com

## Community

I'm a community manager for [Fancy Games](https://store.steampowered.com/publisher/fancy),
overseeing [Escape The Backrooms](https://store.steampowered.com/app/1943950/Escape_the_Backrooms/). Join
our [Discord server](https://discord.gg/fancygames)!  
I also own and run the Escape the Backrooms Community
organisation [GitHub](https://github.com/EscapeTheBackroomsCommunity) | [Codeberg](https://codeberg.org/EscapeTheBackrooms).

<details>
<summary><b>Organisation repositories</b></summary>

- [autosplitter](https://github.com/EscapeTheBackroomsCommunity/autosplitter) (ASL) - The LiveSplit autosplitter for the
  game, covering versions 5.0+. Auto start, splits on level transitions and cutscenes, load removal, and a paused timer
  in cutscenes, the main menu and on crashes. Based on [uhara](https://github.com/ru-mii/uhara) by ru-mii.
- [UE4SS](https://github.com/EscapeTheBackroomsCommunity/UE4SS) (C++) - Our fork
  of [RE-UE4SS](https://github.com/UE4SS-RE/RE-UE4SS).
- [community-wiki](https://github.com/EscapeTheBackroomsCommunity/community-wiki) - The community wiki: confirmed
  features, suggestion guidelines, templates for level, item and entity suggestions, and a guide to running the game on
  Linux.
- [etb-speedrun-bot-v2](https://github.com/MattFor/etb-speedrun-bot-v2) (Python) - The speedrunning bot behind the
  leaderboards and run verification, "The Watcher", originally by [@Reokin](https://github.com/Reokin). Members link
  their speedrun.com profile and the bot keeps their roles up to date.

</details>
