<div align="center">

[![Website](https://img.shields.io/badge/mattfor.com-cc056b?style=for-the-badge&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAMAAABF0y%2BmAAAAP1BMVEUMDAcqKxhMTCw%2FQCU6OyIfIRMgHxGnpl7FxHTHxna5uGyxsGSzsmmUlFRnZzt4eEXGxXXHxnLAv22gn1rAwHHY7KVrAAABbUlEQVQoz32T0ZbDIAhEgRJpUIxW%2F%2F9bdzRtd592HjzGiyMoIfpXLB89lPmA0i2wZE%2FoPNfoZtkLlJci0ZHPj6wyS9xzxOe%2F0IXSQSm2CfQHPs%2BgI8qVDgNtrX1gh07AiqBKYuXV2vm2ba2vvYPkuUYkySrRbEGwEvUaU6h6EdIqstb3zjZDV71hSqrE1p6vSMk27KsgYeJSVi2GZFqvNDaEneRWlKL36Ss5wKDY0JJ6b%2F0i2XtueH3hY2ItSOYXtvqGrgmGOKX2r3DUDWHB9aoJIe7zDR8fOOt%2BnuohXG2ZtpemO1sEohgZ7drPa2un86dOuGiyXpiqoazlXN7Q5pyuXPpI4t2YJHzmY1UB6O5FtXgAemZYVze83AAcaIy8oPERIcg8aRmJ84boGWPNuNmdUBRli6Srh1Kgl8YhlrNdohWfchiu64ZmCBT7lR4DF20bjrHmGEfEHnE2mmUAEqsqU9JfYQ1dqPz%2Fz%2FADs7MZxJrLqYgAAAAASUVORK5CYII%3D)](https://mattfor.com)

[![Email](https://img.shields.io/badge/mattfor%40relaxy.xyz-a02074?style=flat-square&logo=maildotru&logoColor=white)](mailto:mattfor@relaxy.xyz)
[![Codeberg](https://img.shields.io/badge/codeberg-733b7d?style=flat-square&logo=codeberg&logoColor=white)](https://codeberg.org/MattFor)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-support-465686?style=flat-square&logo=kofi&logoColor=white)](https://ko-fi.com/mattfor)
[![Profile views](https://komarev.com/ghpvc/?username=mattfor&label=Profile%20views&color=1a718f&style=flat-square)](https://github.com/MattFor)

</div>


<div align="center">

<img src="https://icon-marquee.giann.dev/v1/marquee?i=c,cpp,rust,js,py,ts,nodejs,discordjs,mongodb,fastify,html,css,opengl,sdl,bash,linux,voidlinux,raspberrypi,podman,git&width=800" alt="C, C++, Rust, JavaScript, Python, TypeScript, Node.js, discord.js, MongoDB, Fastify, HTML, CSS, OpenGL, SDL, Bash, Linux, Void Linux, Raspberry Pi, Podman, Git" />

</div>

I write things that people use.  
C, C++ and Rust are my preferred languages; JavaScript and Python are the ones I use most and know best. Currently
studying in university.

I'm open to collaboration and contributions.  
Everything below is built and maintained in my free time.

---

## My Best projects

### Relaxy! Ecosystem

Everything `relaxy.xyz` related: the bot, the dashboard, the website and the supplementary services.  
A single RaspberryPi hosts everything isolated under Podman and bubblewrap.
<!--  <a href="https://voidlinux.org/"><img src="https://img.shields.io/badge/-478061?style=flat-square&logo=voidlinux&logoColor=white" height="15" style="vertical-align: 0px;"></a> -->

[![relaxy.xyz](https://img.shields.io/badge/relaxy.xyz-0e75b6?style=flat-square)](https://relaxy.xyz)
[![dashboard](https://img.shields.io/badge/dashboard-0e75b6?style=flat-square)](https://dashboard.relaxy.xyz)
[![uptime](https://img.shields.io/badge/uptime-0e75b6?style=flat-square)](https://uptime.relaxy.xyz)
[![cdn](https://img.shields.io/badge/cdn-0e75b6?style=flat-square)](https://cdn.relaxy.xyz)
![|](https://img.shields.io/badge/-6e7681?style=flat)
[![users](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Frelaxy.xyz%2Fstatus.json&query=%24.bot.totalUsers&label=users&style=flat-square&color=2ea043)](https://uptime.relaxy.xyz)
[![lines of code](https://img.shields.io/badge/LOC-~250k-0e75b6?style=flat-square)](https://github.com/MattFor/relaxy-public-v2)

<details>
<summary><b>Relaxy! Discord Bot</b></summary>

A multipurpose Discord bot running as a sharded fleet with one supervising manager process and N cluster processes.
Backend uses MongoDB.

Uses: Node.js v24+, discord.js v14, MongoDB (Mongoose), discord-hybrid-sharding, discord-player (custom fork),
node-canvas, ffmpeg, tesseract-ocr.

- 210,000+ users
- 192 commands, 58 event handlers
- Diff-based document storage, multi-process DB workers, local caching
- OCR-backed and perceptual-hash scam detection on posted images
- Cross-server role sync, ban appeals and synced moderation over a credential-less handshake
- One shared implementation behind every moderation action, for the usual moderation, dashboard as well as linked
  servers
- Hot reload, rolling restarts and class patching
- Shard, network and file watchdogs

[![source](https://img.shields.io/badge/public%20source-half--open-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/relaxy-public-v2)

</details>

<details>
<summary><b>Relaxy! Dashboard</b></summary>

Web dashboard for the bot. Discord OAuth login, three access tiers computed from the OAuth guilds permission bitfield.
Has per-user profile customization as well.

Uses: Fastify, the native MongoDB driver, JavaScript, esbuild.

- Discord OAuth-based access control with three permission tiers, per-request authorization checks, per-session CSRF
  protection and a strict list of modifiable fields

</details>

<details>
<summary><b>Relaxy! Website</b></summary>

The bot's showcase site, plus the public uptime page. I've designed it from the ground up to be as fast as possible.

Uses: HTML, CSS, JavaScript.

- 12 pages, ~4,600 lines of JS, ~5,850 lines of CSS
- Changelog, devlog, technical writeup, CDN, Matrix and Minecraft pages
- The uptime page is driven by the health feeds published below

[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/relaxy-website)

</details>

<details>
<summary><b>Relaxy! Additions</b></summary>

The scripts and services that ensure maximum possible uptime. Written for runit on Void.

Uses: Node.js, POSIX shell scripts, nftables, runit.

- Probes 24 services on a ten-second loop and publishes three JSON feeds (one full, one public, one status)
- Hardware watchdog that pets `/dev/watchdog`, so the Pi reboots automatically on a deadlock
- An uptime ledger with day buckets, incident detection and cause inference, mirrored into a Discord outages channel
- `incident` CLI tool for declaring and annotating outages
- Scripts to keep sshd at the top of the CPU, IO and OOM priority lists, with a self-contained nftables table putting
  SSH in band 0 at DSCP CS6 to ensure the Pi stays reachable while it is dying
- error pages generated from the dashboard's own CSS, so I don't have to write new ones by hand every time I change
  something

[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/relaxy-additions)

</details>

### Emoji Mixer

[![npm](https://img.shields.io/npm/v/emoji-mixer?style=flat-square&color=cb3837&logo=npm&logoColor=white)](https://www.npmjs.com/package/emoji-mixer)
[![PyPI](https://img.shields.io/pypi/v/emoji-mixer?style=flat-square&color=3775A9&logo=pypi&logoColor=white)](https://pypi.org/project/emoji-mixer/)
[![crates.io](https://img.shields.io/crates/v/emoji-mixer?style=flat-square&color=dea584&logo=rust&logoColor=white)](https://crates.io/crates/emoji-mixer)
[![JSR](https://img.shields.io/jsr/v/@mattfor/emoji-mixer?style=flat-square&color=f7df1e&logo=jsr&logoColor=black)](https://jsr.io/@mattfor/emoji-mixer)
[![Go](https://img.shields.io/badge/go-reference-00ADD8?style=flat-square&logo=go&logoColor=white)](https://pkg.go.dev/github.com/MattFor/emoji-mixer/v2)
[![Packagist](https://img.shields.io/packagist/v/mattfor/emoji-mixer?style=flat-square&color=f28d1a&logo=packagist&logoColor=white)](https://packagist.org/packages/mattfor/emoji-mixer)
[![RubyGems](https://img.shields.io/gem/v/emoji_mixer?style=flat-square&color=e9573f&logo=rubygems&logoColor=white)](https://rubygems.org/gems/emoji_mixer)
[![NuGet](https://img.shields.io/nuget/v/EmojiMixer?style=flat-square&color=004880&logo=nuget&logoColor=white)](https://www.nuget.org/packages/EmojiMixer)
[![CI](https://img.shields.io/github/actions/workflow/status/MattFor/emoji-mixer/ci.yml?style=flat-square&label=CI&logo=githubactions&logoColor=white)](https://github.com/MattFor/emoji-mixer/actions/workflows/ci.yml)
[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/emoji-mixer)

Library that generates Google Emoji Kitchen combination image URLs from two emojis, for JavaScript/TypeScript (npm and
JSR), Python, Rust, Go, PHP, Ruby and C#.

Uses: TypeScript, Python, Rust, Go, PHP, Ruby, C#, GitHub Actions.

- 125,000+ total downloads ([npm-stat](https://npm-stat.com/charts.html?package=emoji-mixer))
- 1,221 dependent repositories on GitHub
- 619 base emojis, 330,640 valid combinations
- Compact compatibility data is 2.9MB (OG was 96MB!), shared by all nine packages
- Every package is tested against the same cases and published from one release workflow

### LogEye

[![PyPI](https://img.shields.io/pypi/v/logeye?style=flat-square&color=3775A9&logo=pypi&logoColor=white)](https://pypi.org/project/logeye/)
[![Python](https://img.shields.io/pypi/pyversions/logeye?style=flat-square&color=0e75b6)](https://pypi.org/project/logeye/)
[![CI](https://img.shields.io/github/actions/workflow/status/MattFor/logeye/ci.yml?style=flat-square&label=CI&logo=githubactions&logoColor=white)](https://github.com/MattFor/logeye/actions/workflows/ci.yml)
[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/logeye)

Runtime introspection logger for Python. Reports variable assignments, mutations and function calls as they happen, with
no debugger and no instrumentation of the target code beyond a decorator.

Uses: Python 3.8+, sys.settrace introspection.

- 10,000+ PyPI downloads
- ~5,600 lines across 12 modules, with 21 test modules and 10 demos, tested on Python 3.8 to 3.14 on Linux, macOS and
  Windows
- Educational mode rewrites output into plain sentences for teaching
- Tracks locals, attribute writes, container mutations, arguments and return values

### Lexiglance

[![AppImageHub](https://img.shields.io/badge/AppImageHub-listed-0e75b6?style=flat-square&logo=linux&logoColor=white)](https://appimage.github.io/lexiglance/)
[![Release](https://img.shields.io/github/v/release/MattFor/lexiglance?style=flat-square&color=3775A9)](https://github.com/MattFor/lexiglance/releases)
[![License](https://img.shields.io/badge/license-MIT-0e75b6?style=flat-square)](https://github.com/MattFor/lexiglance/blob/master/LICENSE)
[![CI](https://img.shields.io/github/actions/workflow/status/MattFor/lexiglance/ci.yml?style=flat-square&label=CI&logo=githubactions&logoColor=white)](https://github.com/MattFor/lexiglance/actions/workflows/ci.yml)
[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/lexiglance)

System-wide pop-up dictionary for Linux (X11) and Windows.  
Hold a key combination and point at a word in any
application to see its definitions. Same dict format as [Yomitan](https://yomitan.wiki/).

Uses: C++26, Qt, AT-SPI / UI Automation, PaddleOCR and Tesseract.

- Japanese, Russian, Ukrainian, Korean and Greek, with deinflection (食べさせられなかった finds 食べる)
- Reads text through accessibility interfaces, or with OCR in games, images and videos
- Dictionaries compiled into memory-mapped indexes
- Pronunciation audio, Anki cards through AnkiConnect, and configurable popup themes
- Listed in the official [AppImageHub](https://appimage.github.io/lexiglance/) catalog

### Simple Project Tracker

[![Python](https://img.shields.io/badge/python-3.11%2B-3775A9?style=flat-square&logo=python&logoColor=white)](https://github.com/MattFor/simple-project-tracker)
[![License](https://img.shields.io/badge/license-MIT-0e75b6?style=flat-square)](https://github.com/MattFor/simple-project-tracker/blob/master/LICENSE)
[![CI](https://img.shields.io/github/actions/workflow/status/MattFor/simple-project-tracker/ci.yml?style=flat-square&label=CI&logo=githubactions&logoColor=white)](https://github.com/MattFor/simple-project-tracker/actions/workflows/ci.yml)
[![source](https://img.shields.io/badge/source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MattFor/simple-project-tracker)

CLI project tracker with Git repo discovery, search/filtering, bulk editing, configurable output, and a background
update daemon.

Uses: Python 3.11+.

- ~11,600 lines across 45 modules, with 23 test modules
- 15 commands, each with aliases and a fused short version
- Frecency-based name resolution
- Undoable edits, tui, a background daemon, shell completion for bash, zsh and fish, and a `man` page
- The v1.3.0 project browser was selected for the [XERJ](https://github.com/xerj-org/xerj) Corpus Hub of reference code
  solutions for coding agents

---

## Other projects

- [abba](https://github.com/MattFor/abba) (C++26) - Arbitrary Binary Behavioural Anticheat. Memory scanning, file
  integrity hashing and INI-driven configuration. Still work in progress!
- [von-neumann-machine-simulator](https://github.com/MattFor/von-neumann-machine-simulator) (Rust, egui/eframe) - Von
  Neumann architecture simulator with a native GUI.
- [ibus-mozc-system](https://github.com/MattFor/ibus-mozc-system) (Python, Shell, X11) - Scripts and config that make
  Japanese input under IBus and Mozc work on a keyboard without dedicated JP keys.
- [xfce-tiler](https://github.com/MattFor/xfce-tiler) (Python, X11) - Quadrant, half and directional window tiling for
  XFCE and xfwm4.
- [x11-mic-monitor](https://github.com/MattFor/x11-mic-monitor) (Python, X11, PipeWire) - Hear your own microphone on
  a mouse button, or record yourself and hear it straight back.
- [discord-profile-studio](https://github.com/MattFor/discord-profile-studio) (Python, Tkinter) - Designer for Discord
  Rich Presence and profile widgets with a live preview. Still work in progress!
- [hprint](https://github.com/MattFor/hprint) (C++23) - Header-only utility for centered terminal headers. Unicode 16
  aware widths (emoji sequences, combining marks, escape codes), UTF-8 borders, any output stream, usable at compile
  time.
- [path-variable-editor](https://github.com/MattFor/path-variable-editor) (Python) - Windows PATH editor that works past
  the 2047-character limit, with backups and a check against other programs' changes before saving.
- [mood](https://github.com/MattFor/mood) (Rust, ratatui) - Log 0-10 mood scores with reasons from the terminal, then
  review them as terminal charts or PNG graphs.
- [download-favourite-discord-gifs](https://github.com/MattFor/download-favourite-discord-gifs) (Python) - Downloads
  exported Discord favourite GIFs, converts to correct formats with magic byte detection.
- [raytracer](https://github.com/MattFor/raytracer) (C++) - Ray tracer following Ray Tracing in One Weekend.
- [libstrangle-dlsym-fix](https://github.com/MattFor/libstrangle-dlsym-fix) (C) - Fork of milaq's libstrangle with the
  `__libc_dlsym` lookup error corrected making OpenGL work again on latest glibc.

<details>
<summary><b>Unreleased</b> - Projects which will probably never see the light of day</summary>

- Local AI Studio (Rust, ratatui) - Super+R popup for quick questions to local models. Shows timing per reply, has
  approval modes, and the model can look at the screen, read selected text, search files and search the web.

</details>

<details>
<summary><b>Personal</b> - Random configs and themes that I use</summary>

- [g-mang-hud-mattfor-edition](https://github.com/MattFor/g-mang-hud-mattfor-edition) (TF2 HUD) - My modification of a
  16+ year old TF2 HUD written in ReScript.
- [.bashrc](https://github.com/MattFor/.bashrc) (Shell) - My .bashrc. System, packaging, media and programming
  utilities, each documented with what it needs installed.
- [gtk-config](https://github.com/MattFor/gtk-config) (CSS) - My GTK 3 and 4 theme for Void.
- [xfce4-notes-plugin](https://github.com/MattFor/xfce4-notes-plugin) (Vala) - Fork of the Xfce notes plugin: opens any
  folder of notes (every folder a window), works well with git and Syncthing, reads legacy encodings, scrolls between notes and
  shows/hides on a shortcut.

</details>

<details>
<summary><b>Archive</b> - University work and older projects</summary>

#### University

- [university-coursework](https://github.com/MattFor/university-coursework) (C, C++, Python, Jupyter) - Everything from
  my Computer Science degree, organised by semester.
- [neural-network](https://github.com/MattFor/neural-network) (C++26) - Feedforward multithreaded neural network written
  from scratch, with a test suite. (also submitted as the final project for algorithms & data structures)
- [visual-sorter-v2](https://github.com/MattFor/visual-sorter-v2) (C++20, OpenGL [GLFW], SDL3 and ImGui) - Twelve
  sorting algorithms drawn one comparison at a time. Performance metrics, graphs and more.
- [emergency-department](https://github.com/MattFor/emergency-department) (C++20, POSIX IPC) - A hospital emergency
  department where every role is a separate process, coordinating purely through message queues, shared memory,
  semaphores and signals. Final project for operating systems class.
- [numerical-methods-labs](https://github.com/MattFor/numerical-methods-labs) (C++) - Numerical methods lab programs.
- [university-dotnet](https://github.com/MattFor/university-dotnet) (C#) - Every exercise from the .NET class.

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
overseeing [Escape The Backrooms](https://store.steampowered.com/app/1943950/Escape_the_Backrooms/) since 2023. Join
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
