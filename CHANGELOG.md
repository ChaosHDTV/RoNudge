# Changelog

## v1.4.3

- Member figures that were misread no longer stay in the statistics: a figure that does not fit the member's
  other readings (deliveries and contributed money only ever rise) is left out, also in the history that
  is already recorded
- A misread member figure was accepted when the reading before it had been unreadable; it is now compared
  with the last figure that is known
- A real jump, such as a large deposit into the corporation bank, is taken over once three readings in a
  row show it
- A member recorded under two spellings of the name is shown as one member

## v1.4.2

- Fixed a crash while saving a corporation reading, which showed up once the members history had grown
  large (after about a day of tracking)

## v1.4.1

- Fixed a crash when anti-AFK was started again after a stop while Fleet Empire tracking was on: stopping
  let Windows unload the text recognition, and the next reading called into it

## v1.4.0

- **Faster contract readings and applications.** The Contracts tab is scrolled as fast as the page
  settles instead of with fixed waits, its text is only read where something has to be found, a route's
  distance is read once and then remembered, and applying goes straight to where a card was instead of
  going through the whole board again
- The "show more" button of a long board is found reliably: only the strip at the bottom of the page is
  read for it (read together with the cards above, its small label was not returned at all)
- A long board no longer keeps the next reading from getting back to the top of the page
- Auto-apply says **why** it applied for nothing (in the status line and on its page): which rule turned
  how many offers away, or that the offers that fit are too large for the room left under the limit
- A company whose name is cut short on a badge ("We Overtake" for "We Overtake This Game") is no longer
  taken for a second company with a second contract
- **Backup and restore** in the dashboard's settings: all settings and everything recorded in one file,
  and back again (the state before a restore is saved first)
- The main window is larger (636 x 744 instead of 556 x 520), so its pages show everything without scrolling
- The dashboard has a **Start / Stop** button in its top bar, the same as in the main window
- The dashboard has the same glass as the main window (it had none). It has no title bar of the system
  any more but its own minimise, maximise and close buttons; the strip with the tabs moves it. Windows
  still sizes, snaps and maximises it like any other window
- Dashboard settings: how solid the cards are on the glass (30 to 100 %)
- Webhook page: the two views are a switch under the title; Fleet Empire page: evenly spaced cards with
  larger figures
- The Fleet Empire page of the main window shows the contracts as well (being hauled, pallets left, pace,
  when it is all done, what auto-apply is doing) and what the tracker is doing; its Overview and Settings
  buttons are gone, the dashboard button remains
- Webhook, Log events: only the list of what gets logged; the address is set on the Webhooks view
- Auto-apply: **quiet times** (only with a set number of members online, only between set hours) and
  **swapping** the weakest waiting application for an offer that is clearly better
- The pictures of the balance, the reputation and the corporation bank for Discord have the look of the
  dashboard: a row of tiles with the headline figures (for the balance: income per hour with and without
  interest and when the target is reached; for the corporation: the day's change, the average per hour
  and the day's lowest and highest) and the graph in a card
- The two contract pictures for Discord follow: the overview has a second row for the last 24 hours
  (pallets hauled, earned for the haulers, contracts finished, pace needed) and rounded bars; every
  contract being hauled is a card with its progress large, a bar that turns amber when it will be late,
  and the time left and the verdict as pills
- The members picture for Discord is new: ordered by the money contributed in the last 24 hours, with the
  day's totals on top, a bar per member for the day's contribution, the first three set apart, rank tags
  and the share of the day online. The dashboard's members table sorts by money contributed by default
- **Export** in the dashboard's settings: contracts, earnings by day, members and applications as CSV

## v1.3.0

- Fleet Empire contracts are told apart: what the corporation **hauls** ("You're hauling", also freight of
  its own businesses) and what it **posted** for others, with the company that picked it up. The Companies
  view shows both directions: whom the corporation hauled for, and who hauled for it
- Always on top of the Contracts tab: how many contracts the corporation is hauling right now, the pallets
  left, the first deadline, the pallets hauled per hour and whether that pace finishes every contract in time
- New **Pace** view: pallets hauled per hour over time with the members online underneath (the names on
  hover), the pace needed to finish in time, and the corporation's pace while each member was online against
  the rest of the time. The pace is recorded from this version on
- The "We haul" view shows for every running contract the pallets left, its own pace, the time left and
  when it will be done at that pace
- Fleet Empire can **apply for contracts by itself** (off unless switched on, in the "We haul" view): it
  keeps a set number of contracts going (hauled plus applied for) and applies for the best-paying offers
  of the open board that fit your rules: contract types, the haulers' share, distance and size. It
  presses Apply a second time when the first press did not take, and leaves a company alone for three hours when the game refuses
- Contracts: a pay per pallet the page reading missed is read again on its own, a "$" read as a digit is
  corrected from the total, and tanker freight paid in dollars and cents no longer inflates the total
- New **Auto-apply** view in the Contracts tab: the rules as switches and steppers, and a record of every
  application (the tracker's and the ones made by hand) with what became of it: waiting, accepted, not
  chosen or refused by the game, with the share accepted and the hauler pay of the accepted contracts
- Fleet Empire now only works while anti-AFK is started: the Start button and the Start / Stop hotkey
  start and stop everything at once (this can be switched off in the dashboard's top bar). The same button
  there **pauses** every reading, Discord post and application; the "Read now" buttons still work
- Auto-apply has a **smallest size**: contracts with fewer pallets are left alone
- Auto-apply, more rules: a limit on the **pallets still open** over all contracts as an alternative
  to the number of contracts (a switch chooses which of the two counts), a **minimum time left on the board** to skip offers that have been up for
  a while, and **withdrawing** the tracker's own application when the poster has not answered after a set
  time. An offer given up on is not applied for a second time
- The record of applications shows every contract in full (route, distance, type, pay per pallet, total,
  share) and how long it waited. An offer is told apart by the time it leaves the board, so a refusal that
  is tried again stays one entry that counts the attempts; refusals survive a restart of the app
- Contracts reading: the "show more" button of a long board is found also when its label is misread, the
  time left on the board is read where it was missed before, offers whose time has run out are shown as
  expired and never applied for, and a misread arrow no longer turns "Kansas" into "Arkansas"
- The pace also counts **distance**: pallet-miles per hour (pallets times the miles of their contract), so
  a long route is not mistaken for slow hauling and a short one does not inflate the figure. The Pace view
  switches between pallets and pallet-miles, and "done in" is worked out from the pallet-miles left
- A contract that disappears while its time had not run out counts as **finished** with all its pallets
  (the game removes it before it ever shows 100 %); one whose time ran out counts as late. "We haul" says
  which and when, and the Companies view shows per company how many contracts were finished and when the
  last one was
- Distances: the figure is read once more with its characters moved apart, which keeps a digit between
  two others from being lost ("765 mi" read as 76); a "$" read as "5" in the pay is recognised without
  the total as well
- **Contracts on Discord**, through a webhook of their own (Webhook page, fourth card): one post with the
  overview (contracts being hauled, pallets left, pace in pallets and pallet-miles per hour, when it is all
  done, the pace over the last 24 hours and the day's totals) and below it a post with every contract
  being hauled: route, pay, share, a progress bar, what is left, time left and when it will be done, plus
  the offers applied for. Both are kept up to date or posted anew with each reading
- Contracts reading: the tab bar of the Corporation page is read word by word and the tracker checks that
  the Contracts page really came up (a click that went astray is repeated); the "show more" button is
  found from "MORE" with a count beside it, and the reading says so when the board lists more offers
  than were reached
- The dashboard has a **Settings** tab with everything for Fleet Empire in one place: when the tracker
  works, what it reads and how often, the forecast target, and the three Discord posts with their
  webhooks. The Settings button of the Fleet Empire page in the main window opens it
- **Stop** (and pausing) now also ends a reading that is under way: the tracker lets go of the game at its
  next step instead of finishing the corporation, the contracts and the applications first
- Companies can be set up by hand (click one in the Companies view): **correct its name**, which then
  also applies to everything read of it later, and choose whether auto-apply takes its offers **first**
  or **never**. The view also shows how many applications each company accepted
- Auto-apply can rank the offers by pay per pallet, per pallet-mile or per trip of your truck
- New **Earnings** view: what the hauling paid day by day, with pallets, pallet-miles, contracts finished
  and the earnings per measured hour
- Discord **news** as they happen (application accepted, contract finished or out of time, a contract that
  will not make it at the present pace, a member away for three days) and a **daily summary** with the
  first reading of a day; both are switched on in the dashboard's settings
- A pay per pallet far above everything else on the board with a "5" in front is recognised as a misread
  dollar sign
- The settings rows of the Fleet Empire page in the main window are gone; they live in the dashboard

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
