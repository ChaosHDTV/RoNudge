# Changelog

## v1.2.0

- Fleet Empire: bank interest follows the game's new rule (interest only on the first $50M of the banked balance; the limit is read from the Bank page). Forecast, "income with interest" and the Discord post use it.
- Fleet Empire contracts: distances and pay per pallet that lost a digit when read ("659 mi" shown as 69, "$1,647" as $7) are now caught: the pay is checked against the total, and a route keeps one distance for all its contracts. A contract recorded twice because of such a misreading is folded back into one.
- Fleet Empire: the balance is also read when the Bank page was left on Financial Overview or Financial Management.
- Fleet Empire: before a reading the Roblox window is brought to the size the game needs to show everything (at least 1588 x 1009 inside the window; moved to fit, maximised on smaller screens). A window that is still too small is not read instead of recording wrong numbers. When the tabs of the Corporation page do not all fit and scroll sideways, the tracker scrolls them itself.
- Fleet Empire: the corporation's figures can be posted to Discord through their own webhook: reputation,
  bank, seats and who is online, with graphs of reputation and bank and the whole members table, either as
  one post that is kept up to date or as a new post per reading
- The **Webhook** page has a second view, **Webhooks**, with one card per webhook: the log
  (notifications), the personal balance and the corporation stats. Each shows the address in use with its
  secret part hidden, can have a webhook of its own, and has a test button
- Fleet Empire: members can be corrected by hand in the dashboard (right-click a member, or the button on
  their page): rename, merge into another member, or remove with its history
- Fleet Empire: the corporation post has a larger picture each for reputation and for the corporation
  bank, with the current figure, the change over 24 hours and the average per hour; the personal balance
  shows the income per hour both with and without the bank interest, in the app and on Discord
- Fleet Empire **contracts**: the corporation reading also goes through the Contracts tab. The dashboard's
  new Contracts tab lists the open board sorted by vehicle type and company, the corporation's own
  contracts with their progress, and the companies it has hauled for, with pallets and earnings
  The open board can be sorted by any column and filtered by vehicle type and cargo, and shows pay per
  pallet-mile and the pay per trip for a chosen truck (the list of trucks is a text file you can extend)
- The dashboard window has the app icon and follows the blurred-background setting
- Main window: settings rows are rounded cards and the Start button is a rounded button

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
