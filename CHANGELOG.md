# Changelog

## v1.1.1

- Fleet Empire: in-game notifications that slide over the members table can no longer end up as members.
  A row only counts when its rank cell holds a rank; when rows are covered, the page is read again a few
  seconds later, and a row that stays covered is matched to the known member by its figures or left out
- Fleet Empire: a delivery or contribution figure far from the member's previous one is recorded as
  unknown instead of believed; rows recorded through a notification by v1.1.0 are ignored

## v1.1.0

- Anti-AFK now takes focus more reliably, and never sends input when Roblox could not be focused; such a
  cycle is reported as failed in the status card, the statistics, the tray tooltip and the Discord webhook
- New **Session** page: stop anti-AFK after a set running time, optionally closing Roblox or putting the PC
  to sleep; save and load settings profiles
- Updates install from inside the app: the download is verified against its published SHA-256 first
- Reconnect notifications on Discord include a screenshot of the Roblox window
- Tray tooltip shows the state, the time to the next action and the number of Roblox instances
- Accent colour can be chosen on the Interface page
- Help on hover also works inside the settings sub-pages
- Settings export and import include blur transparency, accent colour and the session limit
- New **Fleet Empire** page for the Roblox game of that name. It works from screenshots of the game window
  and ordinary clicks; nothing is injected into the game
  - Reads the banked balance on a schedule (from every minute), keeps a history, and forecasts when a
    target is reached from the measured income and the bank interest. The target can be set freely
  - Posts the balance graph to Discord, as one post that is kept up to date or as a new post per reading,
    optionally through its own webhook
  - Reads the corporation's main page on its own schedule: name, reputation, corporation bank, seats and
    the whole members table
  - A dashboard window with tabs for balance, corporation and members: graphs that can be zoomed and
    moved, trend forecasts for reputation and corporation bank, a sortable members table with deliveries
    and contributions gained over a chosen period, the share of readings in which each member was online,
    who joined or left, and graphs per member
  - Optional blocking of your own mouse and keyboard for the few seconds a reading works in the game
    window (Esc ends it at once)
  - Needs the English text recognition that ships with Windows 10 and 11

## v1.0.0

First release.

- Sidebar layout with labelled navigation and a live status card
- Anti-AFK with configurable interval, action and timings
- Multi-instance support with an instance manager
- Window tools: hide/show, opacity, grid layout
- FPS/CPU limiter, RAM cleaner, mute
- Auto-start, auto-reconnect, macros, global hotkey
- Status overlay and Discord webhook notifications
- Solid background by default; optional blurred background with adjustable transparency
- Help on hover for every setting, with the full text on click
