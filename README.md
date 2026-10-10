<p align="center">
  <img src="assets/logo.png" width="96" alt="RoNudge logo">
</p>

<h1 align="center">RoNudge</h1>

<p align="center">Keeps Roblox sessions from being kicked for inactivity.</p>

<p align="center">
  <img src="assets/main.png" width="556" alt="RoNudge main window">
</p>

RoNudge sends a small input to each Roblox window on an interval so the 20-minute idle kick never triggers,
and adds the tools you want around that. One exe, no installer, nothing else to install.

## Download

Get `RoNudge.exe` from the [Releases](../../releases) page. This is the only official download. Each
release lists the SHA-256 of the exe so you can check a copy before running it.

## Features

- **Anti-AFK** with a configurable interval and action (jump, W/S, zoom), plus fine-grained timing control
- **Multi-instance** support, with an instance manager and per-instance settings
- **Window tools**: hide/show, opacity, grid layout across monitors
- **Resource savers**: FPS/CPU limiter, RAM cleaner, mute
- **Automation**: auto-start when Roblox opens, auto-reconnect, macros, global hotkey
- **Status overlay** and **Discord webhook** notifications
- **Interface options**: solid or blurred background with adjustable transparency, animations, always on top

## Using it

1. Start RoNudge and open Roblox.
2. Pick an interval and action on the **General** page.
3. Press **Start**. The sidebar shows the live status; closing the window keeps RoNudge in the tray.

Every setting has a **?** button: hover it for a short description, click it for the details.

### Discord webhook

No Discord application or bot is needed. In Discord open the channel settings, then **Integrations**,
**Webhooks**, **New Webhook**, copy its URL and paste it on the **Webhook** page.

## Problems and ideas

Use the [issue tracker](../../issues) of this repository.

## Licence

RoNudge is free to use but not open source: you may not modify, redistribute or reuse it. See
[LICENSE.txt](LICENSE.txt), which also carries the notice for the MIT-licensed code it contains.
