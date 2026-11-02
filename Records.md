# RiskCells Records

RiskCells Records is the trading journal inside RiskCells. This manual covers version 1.2.0. RiskCells Trading has its own manual in the [readme](readme.md).

## Contents

- [About Records](#about-records)
- [Importing trades](#importing-trades)
- [Journaling](#journaling)
- [Pages & cells](#pages--cells)
- [Records MCP](#records-mcp)
- [Data & backup](#data--backup)
- [Features](#features)
  - [Main Bar](#main-bar)
  - [Pages](#pages)
  - [Cells](#cells)
  - [AnalyticsCells](#analyticscells)
  - [JournalCells](#journalcells)
  - [TheStemCell](#thestemcell)
  - [Filters](#filters)
  - [Tags](#tags)
  - [Trades](#trades-1)
  - [Screenshots](#screenshots)
  - [Recordings](#recordings)
  - [Controls](#controls-1)

## About Records

#### What is RiskCells Records?

RiskCells Records is the trading journal inside RiskCells. You import your trades from your platform or prop firm, then tag them, rate them, write your prebriefs and debriefs, add screenshots and session recordings, and study the results on pages you build yourself from cells: curves, pies, bars, statistics, trade lists, calendars and distributions. It runs in its own windows beside your trading, on the same licence.

#### Is Records included in my plan?

Yes. Every plan includes RiskCells Records and the Records MCP server: the Individual plan, the Lifetime licence and every Enterprise seat. There is no separate tier and nothing extra to buy.

#### How do I open Records?

Open the Window Picker in RiskCells. Below your trading windows sits the RiskCells Records BETA section, with one row per journal. Tick a journal to open it, untick it to close every window of that journal.

Records and RiskCells Trading run side by side. When both are open and you close one of them, RiskCells asks whether to close that one alone or both.

#### Can I keep more than one journal?

Yes, as many as you like. Every journal keeps its own pages, filters, imported files, tags, notes, screenshots, look and settings, so you can keep accounts, strategies, evaluations or years completely apart. CONTROLS › JOURNALS opens, duplicates, renames, exports and deletes them, and NEW WINDOW opens another journal beside the one you are in.

#### Can I use Records across several monitors?

Yes. Drag any page tab off the bar and that page opens in a window of its own, where you let go. Drop it on another monitor and it fills that monitor. The windows of a journal stay in step: a trade picked in one window is picked in the linked cells of the others too. Right-click the tab and choose Combine to bring the page back.

#### Where is my journal stored?

On your computer, inside RiskCells. Your trades, tags, notes, screenshots and settings are never uploaded to us. By default nothing leaves your machine, and you stay in control of the rest: the Cloud Folder is a local copy in a folder you choose, which reaches a server only if you put it somewhere that syncs. A YouTube recording plays from YouTube and sends no trading data out. An AI agent on a cloud model sends what it reads to its provider, while a local model keeps it all on your machine.

#### What happens to my journal if my licence ends?

It stays on your computer, untouched. While RiskCells is locked the Records window cannot be edited, but the lock screen keeps one link for you: Export your data. It needs no sign-in, and it gives you the trades of any journal as a CSV and each journal's settings file as JSON. Subscribe again and everything is exactly where you left it.

## Importing trades

#### Which platforms can I import from?

Sierra Chart, Rithmic R | Trader Pro, MotiveWave, Topstep (TopstepX) and TradeCraft. Each has its own importer, built around that platform's own export, so positions come back as whole trades from flat to flat and every import keeps its accounts.

#### How do I import my trades?

Open CONTROLS › IMPORT AND EXPORT.

1. Under Imports Land In, choose the journal the trades go into.
2. Under Platform, choose where the file comes from.
3. Under Times In File, choose the zone the file's times are written in, for times that do not carry their own.
4. Press CHOOSE FILES or CHOOSE FOLDER, or drop the files onto the drop area.

Each file becomes one import, listed under IMPORTED FILES with its trades, accounts and dates. A file dropped anywhere on the page is read as the platform you picked there, and a Sierra Chart trades list is recognised by itself.

#### How do I import from Sierra Chart?

1. In Sierra Chart open Trade › Trade Activity Log and select the Trades tab.
2. Set Profit/Loss (P/L) Format to Currency Value, and leave Use Commission unchecked so the file carries the gross P&L.
3. Make sure these columns are shown, in any order: Symbol, Trade Type, Entry DateTime, Exit DateTime, Entry Price, Exit Price, Trade Quantity, Max Open Quantity, Max Closed Quantity, Profit/Loss, Max Open Profit, Max Open Loss, Commission and Account.
4. On the Trade Activity Log's menu choose File › Save Log As. The file is a .txt.
5. In Records, choose Sierra Chart as the Platform and import the file.

Sierra writes its times without a zone, so set Times In File to the zone Sierra is set to (Global Settings › Time Zone). Group Flat To Flat, ticked by default, joins the legs of one position into one trade, cut where Sierra marks the leg that ends flat.

#### How do I import from Rithmic R | Trader Pro?

1. In R | Trader Pro open File › Orders History (one day per export), or Recent Orders.
2. In Completed Orders, add the columns Qty Filled and Order Number: right-click a heading and choose Add/Remove columns.
3. Export the .csv.
4. In Records, choose Rithmic R | Trader Pro as the Platform and import the file.

The export holds fills, not P&L. Records builds the trades from flat to flat and works out each P&L from the prices and the instrument's tick size and tick value. For a product in Records' contract table those values are filled in for you and wait in CONTROLS › INSTRUMENTS for you to confirm. For any other, type them in there.

#### How do I import from MotiveWave?

1. In MotiveWave open the Account tab at the bottom left, then Trades.
2. Press Export, above the list on the right. The file is a .csv of your executions.
3. In Records, choose MotiveWave as the Platform and import the file.

Records builds the trades from flat to flat and works out each P&L from the prices and the instrument's tick size and tick value, set in CONTROLS › INSTRUMENTS. MotiveWave's times carry their own UTC offset. It writes at most 2,000 executions to a file unless its Trade History settings raise that limit.

#### How do I import from Topstep?

1. In TopstepX open the Trades tab (not Orders) and press Export at its bottom right.
2. Pick the dates and export. The file is called trades_export.csv.
3. In Records, choose Topstep as the Platform. The file does not name its account, so type the account's number into Account Number.
4. Import the file. Its trades land in that account.

Every account keeps its own import, so each account's trades_export.csv can keep its name. You can change an import's account later, in its row under IMPORTED FILES. Topstep's P&L is gross, so the commissions you set in Records are the ones that count. Group Flat To Flat, ticked by default, joins the lots of one position into one trade.

#### How do I import from TradeCraft?

1. In TradeCraft open Settings › Export and export your trades. The .csv holds every trade with one column per tag.
2. In Records, choose TradeCraft as the Platform. Times that carry their own offset are read as written; for any that do not, set Times In File to the time zone of TradeCraft's General Settings.
3. Import the file.

Your tags and ratings come with it. The file does not say which group a tag belonged to, so new tags arrive un-grouped: drag them into tag groups in CONTROLS › TAGS & TAG GROUPS and they appear in the journal. If your export lists every leg as a row of its own, tick Group Flat To Flat before you import.

#### What does Group Flat To Flat do?

Platforms often write one position as several rows: one per leg, per lot or per fill. With Group Flat To Flat ticked, Records joins them into one trade from flat to flat, with the sizes added, the prices averaged by size and the P&L added. Unticked, every row stays a trade of its own.

It applies to the next import. It is ticked by default for Sierra Chart and Topstep, and Rithmic and MotiveWave files are always built from flat to flat.

#### What happens if I import the same file twice?

A file imported again under the same name replaces its own import and keeps its place on your pages. So a shorter file with that name takes out the trades it no longer holds: import the full history, or give the new file a name of its own. Removing an import, with the ✕ on its row under IMPORTED FILES, takes its trades off every page. Their tags, ratings and notes stay in the journal and come back if you import the file again.

#### Why does an instrument show 0 ticks, or a P&L of 0?

Records needs an instrument's tick size and tick value to turn prices into ticks and points, and, for files that carry no P&L, into money. Where it can, it fills them in itself from its contract table, checked against the file. Values it filled in show greyed with an ⓘ until you confirm them. Type any that are missing in CONTROLS › INSTRUMENTS.

#### Which time zone are my trades shown in?

The one you choose. Time Zone, in CONTROLS › GENERAL SETTINGS, is the clock the whole journal shows: a city's local time, summer time included, or the times exactly as written. Dates, days, time-of-day slots and time filters all follow it.

Times In File tells Records which zone a file's times are written in when the file does not say so itself. Every import keeps its own, and you can change it later in its row under IMPORTED FILES.

#### Can I add or edit trades by hand?

Yes. Double-click any value in a trade list or on the trade card to change it, or right-click a trade and choose EDIT TRADE to edit every value at once. What you type is kept over the trade's own values: your file is never changed, the trade keeps its tags, notes and screenshots, and Reset edits brings the original values back. + TRADE adds a trade of your own to the day shown.

#### Are commissions included in my P&L?

When you want them to be. Set a commission per contract, round turn, for each instrument or instrument group in CONTROLS › INSTRUMENTS, then switch Commissions on in GLOBAL FILTERS. Every P&L in the journal then shows after commission, and the Comm column shows what each trade paid. Imports from Sierra Chart, Topstep and TradeCraft carry the gross P&L, so the commissions you set in Records are the ones that count.

## Journaling

#### How do I tag a trade?

Pick the trade in Daily trades, or in any trade list, and the Trade & tagging cell shows it beside your tag groups. Click a tag to put it on the trade and click it again to take it off. COPY and PASTE move a trade's tags onto another trade, and CLEAR takes them all off.

#### What are tag groups?

A tag group holds tags of one kind: your setups, your mistakes, your mindset, the market. A tag shows in the journal and in the filters while it sits in a group. Make a group exclusive and only one of its tags can be on a trade at a time, which suits a setup or a market read. A tag you drag out of every group is retired: hidden everywhere, with the trades it was on kept.

#### Is there a ready-made set of tags?

Yes, the STARTER SET: tag groups for Setup, Mistakes, Mindset, Market and Hindsight, plus Day tags such as Good sleep and Big news day. Add it from CONTROLS › TAGS & TAG GROUPS, then rename, recolour or delete anything in it. The same place brings in tags or whole tag groups from your other journals.

#### What are day tags?

A tag can work on single trades, on whole days, or both. A day tag is set once in the debrief, for example Poor sleep or Big news day, and counts for every trade of that day. The filters, splits and statistics then show how your trading changes on the days that carry it.

#### What is signal strength?

Any tag can carry a number, positive or negative, set in its EDIT TAG. A trade's signal strength is the sum of its tags' numbers, its own and its day's. Score your confluences up and your warnings down, then show it under a curve, a bar chart or a distribution, or read it as a column in your statistics and trade lists.

#### How do ratings work?

Rate every trade from 1 to 3 for how well you traded it, and every session from 1 to 3 in the debrief. Ratings have colours of their own, so a curve, pie, bar chart or statistics table split by trade rating or session rating shows at a glance whether your best-executed trades are also your best-paying ones. Unrated trades can show as a group of their own or stay out.

#### What are the prebrief and debrief?

Your notes before and after the session. The prebrief holds your plan. The debrief holds what happened, your session rating and your day tags. There is a prebrief and a debrief for every day, every week and every month, and each can grow into pages of notes, tables, checklists and screenshots. Save one as a template, apply it to any other, or make it the default every new one starts from.

#### Can I add screenshots to my trades?

Yes, as many as you like on every trade, plus strips of their own in every prebrief and debrief. Drop images onto the cell, paste one with Ctrl + V, or press IMPORT (PNG, JPG, GIF and WEBP). The built-in editor puts arrows, lines, shapes, text and other pictures on a screenshot without ever changing the original, and DOWNLOAD saves a copy with your marks drawn in.

#### Can I watch my session recording at each trade?

Yes. Add your recording to the Trade visualiser, either a YouTube video (unlisted works, with embedding allowed) or a video file on your computer, and give it the time on its first frame. Pick a trade and the recording goes to a few seconds before its entry. A recording on your computer can also take screenshots by itself for the whole session: at the entry, the midpoint, the exit and every add or partial exit of each trade. A YouTube recording gets none of those, and you can take a frame of it by hand with the SCREENSHOT button.

#### When is a trade breakeven?

When you say so. BREAKEVEN SETTINGS set a range around zero, in ticks or in P&L, and a result inside it counts as breakeven instead of a win or a loss. The range can also be relative, a percentage of your average loss, and can count before or after commissions. Set it for the whole journal in GLOBAL FILTERS, then override it for an instrument group, a page or a single cell. Until you set one, only exactly zero is breakeven.

## Pages & cells

#### How do I build a page?

A page is a canvas you fill with cells. + CELL adds one, you drag it by its bar and resize it, and cells snap to each other and to the page edges as you go. Every cell has its own settings, filters and colours. Make as many pages as you like, colour their tabs, and save any page as a template layout to build new pages from.

#### Which cells can I use?

The analysis cells: Curve, Pie, Bars, Stats, Trades, Calendar and Distribution. The journal cells: Navigator, Daily trades, Prebrief, Debrief, Prebrief-Debrief, Trade & tagging and Trade visualiser. And the StemCell, which runs your own code on your trades. Any cell goes on any page, as many times as you like.

#### How do the filters work?

In three layers. GLOBAL FILTERS apply to every page of the journal, in every window. PAGE FILTERS narrow each page further, and every cell can narrow its page again with filters of its own. Each layer picks accounts, instruments, dates, days and times of day to leave out, and filters by result, side, size, duration, trade rating, session rating, entry and exit order type, and tags.

#### Can I compare my trades by tag, time or instrument?

Yes, that is what a split does. Split a curve, pie, bar chart or statistics table by tag, instrument, instrument group, contract, account, side, result, time of day, weekday, rating, order type, size or duration, and it draws one curve, slice, bar or row per value. Add a second split inside the first, for example each setup by time of day.

#### What is the StemCell?

Your own study, written in JavaScript and run on the cell's trades after all of its filters. Write it, paste it, drop in a .js file or have your agent write it, and the cell shows whatever it makes: tables, text, charts in the journal's colours, or a canvas you draw on. Your code can add fields of its own above its output, such as an account size, and MANAGE CODES keeps a code under a name, to load into any StemCell of any journal.

#### Is code in a StemCell safe to run?

It runs in a sealed box. The code gets the cell's trades and nothing else: it cannot reach the network, the rest of Records, your settings or your licence. A run that takes longer than five seconds is stopped, so an endless loop never freezes the journal. Even so, run only code you trust or understand.

#### Can I change how Records looks?

Almost everything. GRAPHIC SETTINGS cover the font, the corners, frames, cards, glow and blur, the chart grid, the zero line, gradients, axes, the crosshair, and the colours of wins, losses, sides and ratings. Save the look as a theme, load the DEFAULT or GLASS skin, or load a theme file exported from RiskCells Trading. Each cell can also take colours of its own.

## Records MCP

#### What is the Records MCP?

A server inside RiskCells that lets the AI agent you already use work in your journal: Claude Desktop, Claude Code, Codex, Cursor, VS Code, or an agent in a container. Your agent can read your trades and statistics, tag and rate trades, write debriefs, build pages, change settings, highlight trades and take pictures of pages for its reports. What it does shows in your open Records windows as it happens.

#### Does the Records MCP cost extra?

No. It is included on every plan and every seat. The agent itself, such as your Claude or ChatGPT subscription, is a separate product from its own provider.

#### How do I connect my agent?

1. In Records open CONTROLS › AGENTS MCP.
2. Under SET UP YOUR AGENT, choose your Client and press COPY CONFIG.
3. Paste it where that client keeps its MCP servers. The note under the Client row says where, for example Claude Desktop › Settings › Developer › Edit Config.
4. Switch Agent Access ON, then restart the client.
5. Ask it something, for example "What is in my RiskCells journal?"

Every client on this computer starts a small helper that ships with RiskCells and finds the access token by itself, so its configuration holds no secret. An agent in a container connects with the address and the token instead: keep that copy private, and press REGENERATE TOKEN if it was ever shared.

#### What can an agent do, and can I limit it?

Every kind of action has its own switch under WHAT AGENTS MAY DO: journals, pages, cells, tags and notes, trades, instruments and accounts, imports, exports, the look, navigation and media. The everyday actions are on. The destructive ones, such as deleting journals, pages, cells, tags, imports or screenshots, stay off until you switch them on. Agent Access starts off and stops every call at once, and a right-click on the AGENT pill pauses agents.

#### What if an agent deletes something I wanted?

Two safety nets are on from the start. Confirm In App asks you, on a plate in the Records window, before any destructive call runs. Backup Before Every Destructive Task saves what that call can change before it runs, and RESTORE in AGENTS MCP › BACKUPS puts it back. Backups stay in Documents › RiskCells Records › Backups until you delete them, so clear out old ones from time to time.

#### Does my data leave my computer when an agent uses it?

The server listens on this computer only and answers only calls that carry your install's token, so nothing elsewhere can reach it. What your agent reads goes wherever that agent sends it. A model running on a provider's cloud servers sends what it reads to that provider, under its terms, so choose your provider with care. A local model can operate the Records MCP too, and your data then stays on your machine. The ACTIVITY log in AGENTS MCP lists every call an agent made.

Do not put sensitive information such as seed phrases, passwords or login details in your journal. We do not control the agents you connect to it.

## Data & backup

#### How do I back up my journal?

CONTROLS › BACKUP › BACKUP NOW saves everything on this computer in one file, in a folder you choose, under a name you give it. A backup is made when you press the button, and once by itself when a computer that holds data joins a Cloud Folder. RiskCells never changes or deletes one, and an agent can add one but never replace or delete one. RESTORE brings it back as new journals named "FROM BACKUP", so nothing you have is replaced. To get real files you can open, use EXPORT TO A FOLDER in IMPORT AND EXPORT: Settings, Trades, Imported Files, Screenshots and Recordings, each with its own switch.

#### How do I move my journal to another computer?

The simplest way is the Cloud Folder: link both computers to the same folder and they share the same journals, screenshots and recordings, kept up to date both ways. An empty computer just joins, and one that already holds data asks you once how to join. Without it, save EXPORT ALL (JSON) of each journal on the old computer, import it on the new one, and import your trade files there again.

#### What is the Cloud Folder?

A folder you choose, for example inside Dropbox, OneDrive or Google Drive, where RiskCells keeps a copy of everything: every journal with its trades, imports, tags, notes, screenshots and videos, and your RiskCells Trading settings. Another computer linked to the same folder has the same journals, up to date. The agents' token, the Stream Deck token and your sign-in stay on each computer.

Nine switches choose what travels: Journal Data, Pages, Look, Templates, Imported Trades, Live-Log Trades, Screenshots, Video Files and Trading Settings. All are on by default. A delete nobody confirmed stops before it reaches your other computers, and RiskCells asks: KEEP THEM or DELETE EVERYWHERE. See "What is a Big Delete?".

#### What if two computers change the same thing?

The later change wins, by the time it was made, also when one computer had Sync Folder off. The value it replaced is kept under CONFLICTS in CONTROLS › CLOUD FOLDER. RESTORE makes it the journal's value again, on every computer. A Cloud Folder also never mixes two RiskCells accounts: a folder that belongs to another account is refused.

#### What happens when another computer joins my Cloud Folder?

A computer that already holds data shows both sides side by side, its trades, newest trade and screenshots beside your other computers, and asks once. MERGE BOTH keeps everything from both. USE THE CLOUD FOLDER'S DATA makes the journals, pages, looks and settings the folder's. IGNORE changes nothing. Imported trades and screenshots are kept either way, and a backup of that computer is saved first. From then on the two stay in step by themselves, so it does not ask again unless you choose a folder again. An empty computer just joins.

#### What does Confirm Changes For Sync do?

It shows you what changed before anything syncs. The first changes that reach a computer after it starts wait, and you see what changed and on which computer, for example 73 new trades and 12 new screenshots from DESK, with both sides side by side. SYNC NOW brings them in, and TURN SYNC OFF leaves the computer as it is, with the changes waiting. Each computer has its own switch, on by default. Switch it off in CONTROLS › CLOUD FOLDER and changes sync without asking.

#### What happens if I turn Sync Folder off and on again?

Off, your computer carries on from where it is and nothing is sent or received. Changes made meanwhile keep the time they were made. On, each computer sends only what it changed and takes in what the other changed, so nothing goes backwards and no new data is overwritten by older data. It is a pause, not a split: what you did while it was off goes out too, deletes included. With Confirm Changes For Sync on, you see the changes first. COMPARE shows both sides at any time.

#### What is a Big Delete?

A delete nobody confirmed, from an agent, a mistake or a damaged computer, stops before it reaches your other computers. It stops at 5 or more things of a kind within 5 minutes, or when all of a kind go. Imported trades, trades added by hand and whole journals always stop, whatever the number, and so does an import that comes back with fewer trades. RiskCells asks: KEEP THEM or DELETE EVERYWHERE. A delete you confirmed yourself passes.

#### What happens to my windows on a computer with other monitors?

Each computer keeps its own windows: where they are, their size and which ones are open. What travels is what is inside them, so five monitors on one computer and one on the other is fine. Window places only travel between computers whose screens are laid out exactly the same. A window made on the other computer does not open by itself here. If a window's saved place lies on no screen, it moves to the nearest one.

#### What is in the trades CSV?

Every trade in the date range you choose, across all accounts, one row each: account, symbol, instrument, side, size, entry and exit time and price, gross P&L, commission, net P&L, ticks and points per contract, MAE and MFE in ticks, duration, entry and exit order type, rating, tags and note, plus the time zone the times are written in. Dates are written as YYYY-MM-DD, so other programs read them as dates.

#### Can I start a journal over?

Yes, in two ways. NEW JOURNAL in CONTROLS › JOURNALS gives you a fresh, empty journal beside the one you have. DELETE ALL JOURNAL DATA, in IMPORT AND EXPORT, permanently deletes every tag, tag group, rating, note and per-trade value of the journal you are in, and its links to YouTube recordings. Your imported files and your pages are not touched. It asks first, and exporting a backup before you use it is a good idea.

## Features

### Main Bar

#### Journal Name

The name next to the Records wordmark is the journal open in this window. Click it to see all your journals and open another one here, or to start a NEW JOURNAL. Right-click it to rename, duplicate, export or delete the journal, or to open it in a new window.

*Note: Every journal is completely separate: its own pages, filters, imported files, tags, notes, screenshots, look and settings.*

#### Page Tabs

Every page of the journal has a tab on the bar. Click a tab to show its page, double-click it to rename it, and drag it along the bar to put it somewhere else. Right-click a tab for the page's menu: rename, colours, clone, open or save a template layout, reset, open in a new window and delete.

Give a page a colour and its tab carries a small dot of it while the page is in the background, and turns that colour completely while the page is on screen, the same way a tag lights up once it is on a trade. When there are more tabs than the bar can hold, they overlap neatly instead of pushing the other buttons away, and the one under the pointer comes to the front.

#### + PAGE

"+ PAGE" adds a new, empty page. Right-click it to build the new page from one of your saved template layouts instead.

#### + CELL

"+ CELL" adds a cell to the page on screen. Every cell is in the one list, the analysis cells and the journal cells alike, and you can add any of them as many times as you like. A page with journal cells also offers Reset layout here, which puts them back in their default places without touching their settings.

#### PAGE FILTERS

"PAGE FILTERS" opens the filters of every page of the journal, each page as its own section. A page's filters narrow what the GLOBAL FILTERS let through, so every cell of that page only shows that page's trades. The button can show how many trades the page on screen holds (Show Trade Number, in GLOBAL FILTERS).

#### System Clock

A clock on the main bar, from your computer's time. Choose its zone (your computer's, the journal's own, UTC or any city), whether it shows seconds, milliseconds and the date, a 24-hour or 12-hour clock, its colour and weight, and its place, left or right. Click it to open those settings. Switch it on or off in CONTROLS › INTERFACE.

#### AGENT

The "AGENT" pill is the light of the Records MCP. Grey means agent access is off, lit means it is on, and it pulses while an agent is working. Click it to open AGENTS MCP. Right-click it to pause or resume agents, or to clear the trades an agent has highlighted.

#### CLOUD

The "CLOUD" pill shows the state of the Cloud Folder at a glance. Click it to open CLOUD FOLDER, right-click it to pause it or to sync now.

#### GLOBAL FILTERS

"GLOBAL FILTERS" are the journal's own filters. Every page of the journal, in every window, starts from the trades they let through. This is also where the journal-wide settings live: Commissions, the trade count and the light on the PAGE FILTERS button, the BREAKEVEN SETTINGS of the whole journal, and IMPORT FILES.

#### CONTROLS

"CONTROLS" holds every setting of the journal, in groups that open and close on their own: JOURNALS, INTERFACE, GENERAL SETTINGS, GRAPHIC SETTINGS, TAGS & TAG GROUPS, INSTRUMENTS, ACCOUNTS, IMPORT AND EXPORT, AGENTS MCP, CLOUD FOLDER, BACKUP and ABOUT. Each cell keeps its own settings on the cell itself.

#### Quick Dates

The GLOBAL FILTERS can put Quick date buttons on the main bar: TODAY, THIS WEEK, LAST WEEK, THIS MONTH, LAST MONTH and ALL. One click sets the dates of the whole journal, on every page. Tick the ones you want in GLOBAL FILTERS › Quick.

*Note: Inside RiskCells, CONTROLS and GLOBAL FILTERS sit on the window's own bar, next to the Window Picker, like every RiskCells window.*

### Pages

#### Pages

A page is a canvas of cells you arrange yourself. Some traders keep one page for everything. Others keep a page per account, per strategy, per instrument or per review routine: a daily page for journaling, a weekly page for statistics, a page for one prop firm evaluation. There is no limit on how many pages a journal holds, and each one keeps its own filters.

A page that holds journal cells behaves as a journal page: a trade picked there opens in its journal cells, and its curves pulse the picked trade. Every other page is a dashboard. Both are the same kind of page, so you can mix analysis cells and journal cells on one canvas.

#### Template Layouts

"Save Template Layout" keeps the page as it stands, every cell with its place, size and settings, under a name. "Open Template Layout" lays a saved layout onto a page, asking first when the page already has cells, and a right-click on + PAGE builds a new page from one. Manage template layouts renames and deletes them.

*Note: Deleting a template layout never changes the pages built from it.*

#### Pages in Their Own Window

Drag a page tab off the bar and the page opens in a window of its own, right where you let go. Drop it on another monitor and it fills that monitor. "Open in new window" in the tab's menu does the same.

The main window keeps the tab of every page that has been split off, shown at half strength. Click it to bring that window forward, or right-click it and choose Combine to bring the page back. Combine ALL brings every split window home at once.

*Note: Every window of a journal stays in step with the others. Change a setting, a tag or a filter in one window and the others follow.*

#### Canvas Menu

Right-click the empty canvas for the layout tools: Snap to grid, Autosize cells (the cells stretch to fill the canvas), Fit Edges, the window's zoom, Reset layout on a page with journal cells, + Cell, Open and Save Template Layout, and Export or Import settings.

#### Selecting Cells

Drag across the empty canvas to draw a box around several cells, or Ctrl + click a cell's bar to add it to the selection. Selected cells move and resize together. Right-click one of them to duplicate, delete or paste attributes to all of them at once, or MATCH SIZE to give every selected cell the size of that one.

#### Fit Edges

With "Fit Edges" on, the Records window hugs your cells, the way every RiskCells window hugs its cells. It follows every move and resize. With it off, the window keeps its own size and the page scrolls. Double-click the empty canvas to hug the cells again.

### Cells

#### Cell Bar

Every cell has a bar on top. Drag the bar to move the cell, and drop it onto another cell to swap the two. Click the cell's title to open its settings. The square next to the ✕ maximises the cell over the whole page and restores it again, without changing its place or size. Right-click the bar to rename, duplicate or delete the cell, or, on an analysis cell, to copy and paste its attributes.

A name you give a cell is added after its type, so a Stats cell named ES reads STATS ES. You always know what kind of cell you are looking at, and which one.

#### Cell Settings

A cell's settings open in two parts. CELL TYPE and FILTERS holds what the cell is and what it shows: its name, its type, its metric and unit, its split and its own filters. GENERAL SETTINGS holds how it shows it: decimals, legend, markers, values and the like. Any of the AnalyticsCells, and the StemCell, can be turned into another of those types at any time, keeping its size, place, split and filters.

#### Any Setting on the Bar

Almost every row of a cell's settings has a small box at the end of its name. Tick it and that setting appears on the cell's bar, as a switch, a dropdown or a button, so the controls you use all the time are one click away without opening the settings.

This is what keeps a dense page clean. A Calendar can carry its metric and its day chart on the bar, a Curve its metric and unit, a Trades cell its columns. Everything else stays tucked away until you need it.

#### Split

A split draws one curve, slice, bar or row per value instead of one for everything. Split by tag, instrument, instrument group, contract, account, side, result, time, rating, session rating, entry or exit order type, size or duration. Time can be cut into 15 or 30 minutes, 1, 2 or 4 hours of the day, or by day of the week, day, week, month or year.

Add a second split and it splits inside the first, for example every setup by time of day. A split by tag picks which tags count, and can show the untagged trades as a group of their own. A split by rating can show the unrated ones. A curve or bar chart can also show the unsplit total beside the split ones (Show Unsplit).

#### Show on Hover

Bars, Pie and Calendar cells show plates under the pointer, and you choose what goes on them: Stats, Trades, Curve, Instruments, Tags and Times, in the order you pick them. Hover a bar, a slice or a day and you see its statistics, its trades and its curve without opening anything.

#### Copy and Paste Attributes

Right-click the bar of an analysis cell and COPY ATTRIBUTES to take its settings, then PASTE ATTRIBUTES onto another one to give it the same. A set of filters copies the same way between pages, the GLOBAL FILTERS and cells, with a right-click on its name.

#### Duplicate and Copy to Page

"DUPLICATE" makes a copy of the cell with every setting, right beside it. "COPY TO PAGE" puts a copy onto another page of the journal. Both sit at the bottom of the cell's settings.

#### Custom Object Colours

Every cell follows the journal's chart colours until you give it its own. In CUSTOM OBJECT COLOURS any colour of the cell can be switched to a colour of its own, for that cell only, and switched back to the journal's at any time without losing it.

#### Time Blocks

Right-click a point on a curve or a bar chart to mark a time block there: a coloured band across the chart, for a session, a news window or a change in your rules. Drag a block to move it, drag its edge to widen it, and right-click it to recolour or remove it.

#### Linked Cells

The journal cells, and any Calendar or Trades cell you link, follow each other. Pick a day in a linked calendar and the navigator goes to it. Pick a trade in a linked trade list and the trade card and the visualiser show it, and the briefs show its day. This works across pages and across windows.

There are five links, LINK 1 to LINK 5. Right-click the LINKED button on a cell's bar to choose its link. Cells on the same link follow each other, and the other links do not see them, so one page can review today while another holds last week. Switch LINKED off and the cell keeps what it shows until you link it again.

### AnalyticsCells

#### Curve

The "Curve" draws a running figure trade after trade: cumulative P&L, win %, average trade P&L, average MAE, average MFE or drawdown. The X axis runs by trade number or by date, and every value can be read in currency, points or ticks, in total or per contract.

Split a curve and every value gets a curve of its own, so you can lay your setups, your instruments or your sessions over each other and see which one carries the account. A curve can carry the trade distribution under it (Add Distribution), zoomed and panned together with the curve, and the signal strength of each trade (Add Signal Strength).

*Note: In GENERAL SETTINGS a curve can show a dot on every trade (Markers), a line at its latest value (Price Line) with that value tagged on the Y axis (Value Tag), and the room it keeps around itself (Margins).*

#### Pie

The "Pie" shows how something is shared between groups: the number of trades, the contracts, the gross profit, the gross loss, the P&L, the average duration or the signal strength. Its slices print the percent, the value or both, and a donut hole you size yourself leaves room in the middle.

#### Bars

"Bars" draws one bar per group, for any metric the journal measures: P&L by setup, win % by hour, profit factor by weekday, average loss by instrument. Sort the bars by their natural order, by value high to low or low to high, or drag them into an order of your own.

Bars can print their values, show a thin wick for the drawdown and runup of their trades (on an average, the average MAE and MFE), and, when split by time, show the empty time slots too and colour each bar by whether it made or lost money. Every time slot can also carry a colour of its own.

#### Stats

"Stats" is a statistics table with one row per group and an ALL row. Choose the columns from more than thirty measures: the trade count, wins and losses, P&L and commissions, win %, average trade, average winner and loser, profit factor, consecutive winners and losers, drawdowns and runups, biggest win and loss, MAE and MFE, durations, contracts, gross profit and loss, average ratings and signal strength.

#### Trades

"Trades" is a trade list. Choose its columns, show the newest first or the oldest, and read every value in the unit you pick. Linked, a click on a trade picks it for the journal cells. Double-click a value to edit it, and right-click a trade for EDIT TRADE and the rest of its menu.

#### Calendar

The "Calendar" shows a month with a cell per day: its P&L or any other metric, and under it the day's own chart, one bar per trade, the day's curve or a wins and losses pie. Days are tinted by their result, and a week column adds up each week with its number and trade count. The week column has its own Week Chart and Week Tint By Result, and a frame like the days have. The inside of the day and week boxes follows the Calendar colour in CHART BACKGROUNDS, the card around them keeps its colour, and a cell can give its Day boxes and Week boxes colours of their own in CUSTOM OBJECT COLOURS. Hide Saturday and Sunday if you never trade them.

Step through the months with the arrows, and LATEST brings you back to the newest month. Linked, a click on a day opens it in the navigator, a click on a week opens that week, and a click on the month's name opens the month. Unlinked, a day has its own menu.

#### Distribution

The "Distribution" draws one bar per trade, in time order, each its P&L, with thin lines down to its MAE and up to its MFE. It shows what a curve hides: how far each trade went in your favour and against you while you held it.

### JournalCells

#### Navigator

The "Navigator" is the journal's tree: YEARS, MONTHS, WEEKS and DAYS, with the equity curve of what it lists. Click a row to open it, and ◀ Back goes one level up. The list sorts by date or by P&L, its columns are yours to choose, and TOTALS and AVERAGES rows can sit under it.

The navigator holds up to three cards: the list, the chart and the trades of the picked row with their statistics. Drag the cards and the dividers between them to arrange the cell the way you read it. The chart can show the curve, the trade distribution or both together.

*Note: At DAYS an empty row can mark where the week changes, so a long list of days still reads in weeks.*

#### Daily Trades

"Daily trades" shows the day picked in the navigator: statistics tiles across the top and its trades underneath. Choose the statistics and the columns, and add TOTALS and AVERAGES rows under the trades. Click a trade to pick it for the trade card and the visualiser. "+ TRADE" adds a trade of your own to the day.

Ctrl + click several trades of the same account, instrument and direction and right-click them to merge them into one trade. Unmerge splits them again.

#### Trade & Tagging

"Trade & tagging" holds two cards side by side. The trade card shows the picked trade: its account, instrument, entry and exit, P&L, ticks, points, MAE and MFE, duration, legs, its rating from 1 to 3 and your note on it. Choose which rows it shows, and read ticks and points per contract or in total.

The tags card shows your tag groups as cards or as one stack. Click a tag to put it on the trade and again to take it off. COPY and PASTE carry a trade's tags to another trade, CLEAR takes them all off, and CALCULATE STATS shows how the trades that carry the same tags have performed. Switch Sides, or drag a card onto the other, to swap them.

#### Trade Visualiser

The "Trade visualiser" holds everything you can see of the picked trade. IMPORT takes screenshots by drop, paste or file, and session recordings. IMAGES shows its screenshots on two cards, AUTO SCREENSHOTS and IMPORTED SCREENSHOTS. Pick them and drag them into order inside their card. A card with nothing in it does not show. AUTO ORDER, in the cell's settings under Screenshot Order, puts them in the order they were taken. VIDEO plays the session recording at the trade's entry.

#### Prebrief and Debrief

The "Prebrief" holds your notes before the session: the plan, what you expect, what you will and will not trade. The "Debrief" holds what happened, what went well and what to change, with the session's rating from 1 to 3 and the day tags. Both follow the day picked in the navigator, or, unlinked, any day you choose on the small calendar at their top, including a day with no trades yet, like tomorrow's prebrief.

Briefs are not only daily. Pick a week in the navigator or the calendar and the linked briefs show that week's, pick a month and they show the month's. So a weekly review and a monthly review each have a place of their own.

#### Prebrief-Debrief

"Prebrief-Debrief" is both briefs in one cell, with a PREBRIEF / DEBRIEF switch always on its bar. Use it where room is short, or keep the two cells side by side.

#### Brief Pages and Blocks

A brief can hold up to 20 pages, each with its own name and colours. A page is a grid of blocks, up to six across: NOTES for your own words, a TABLE of fields, a CHECKLIST to tick and SCREENSHOTS of its own. Drag a block by its head to another place, onto another block to swap them, or onto a page's tab to move it there.

*Note: Tables take bold, underline and coloured words, and each field can have its own colours. Checklists can run in several columns.*

#### Brief Templates

"SAVE AS TEMPLATE" keeps a brief, its words and its pages, under a name. "APPLY TEMPLATE" puts it into any day, week or month, asking whether to replace what is written or add below it. A default template can be set for daily, weekly and monthly briefs alike: every brief you have not written in yet shows it, and changing the default changes all of those, while every brief you wrote in keeps its own.

### TheStemCell

#### StemCell

The StemCell runs your own study on your trades. Whatever you want to measure that no cell measures yet, a Sharpe ratio on your account size, an expectancy by setup, a custom score, write it in JavaScript and the cell shows the result. Have your agent write it, paste it in, or drop or import a .js file.

The cell has two faces, switched on its bar. SOURCE CODE is where the code is written. OUTPUT is what it makes: tables, text, charts drawn in the journal's own colours and font, or anything you draw on a canvas of the cell's size. Typing runs nothing; the code runs when the pointer comes onto the cell's bar or onto OUTPUT, so the result is ready the moment you look.

#### What Your Code Receives

The code receives the cell's trades after the global, page and cell filters, oldest first, each with its account, instrument, side, size, times, prices, P&L before and after commission, ticks, points, MAE, MFE, rating, session rating, tags, signal strength, note and result. It also receives the tags and tag groups and the journal's colours.

#### Inputs

Your code can ask for its own fields: a number, a switch, a text or a choice, shown in a row above the output. Give it an account size, a risk-free rate or a lookback, change it there, and the study runs again with the new value. The values are kept with the cell.

#### Manage Codes

"MANAGE CODES" keeps a code and its inputs under a name, to load into any StemCell, in this journal or another one. "Load code..." puts a saved one back into a cell, and asks first if the code there is not saved; "Manage codes..." renames or deletes them.

#### The Sealed Box

The code runs sealed off from everything else. It cannot reach the internet, the rest of Records, your settings, your sign-in or the lock screen, and it gets nothing but the cell's own trades. A run longer than five seconds is stopped, so a mistake in a loop can never freeze the journal.

*Note: Only run code you trust or understand. The sealed box protects RiskCells; it cannot tell you whether a study's maths is right.*

### Filters

#### Three Layers

Filters work in three layers, each narrowing the one before it. GLOBAL FILTERS decide which trades the journal shows at all, on every page and in every window. PAGE FILTERS narrow each page. Every cell's own filters narrow its page again. So a page can hold one cell for the whole month next to one for long trades only, both inside the same account choice.

#### Accounts

Pick the accounts a layer shows; none picked means all of them. Click an account for its details, and right-click it to uncheck it or to exclude it, which keeps it in the row while its trades are left out.

#### Instruments

Pick instruments one by one, or a whole instrument group at once. An un-grouped instrument dragged onto a group button joins that group everywhere in the journal. The coloured dots are the colours set in CONTROLS › INSTRUMENTS.

#### Dates and Quick

From and to on one row. An empty "to" runs to the last day on record and moves on by itself, so a filter from the first of the month keeps following the month. Quick sets the dates in one click: today, this week, last week, this month, last month or all.

#### Date and Time Exclusions

Leave out whole days, such as a holiday week, or times of day, such as the open or the lunch hour. Each exclusion is its own row, and a time range may run across midnight.

#### Add Filter

"Add filter" picks a filter by Win / Loss, Long / Short, size, trade duration, trade rating, session rating, entry order type, exit order type or tag. Filters of one kind add up, so a trade matching any of them passes, while different kinds narrow each other. Right-click a filter to duplicate it, exclude what it matches, or mute it for a moment without losing it.

A tag filter matches ONE OF or ALL OF the tags you tick, and can let the untagged trades through too, which is the quickest way to find the trades you still have to tag.

#### Breakeven Settings

"BREAKEVEN SETTINGS" decide when a trade counts as breakeven instead of a win or a loss. Set a range around zero, by ticks or by P&L: with 2 ticks, a stop moved to entry that slipped 2 ticks is breakeven, not a loss. Light up RELATIVE and the range becomes a percentage of the average loss, worked out again as your trades change. Choose whether the range is judged before or after commissions.

Set it for the whole journal in GLOBAL FILTERS. An instrument group, a page or a single cell can override it: a cell's own range comes first, then its page's, then the instrument group's, then the journal's. So a micro contract and a full-size one can each use the range that makes sense for it.

*Note: Until you set a range, only exactly zero is breakeven. Every count of winners and losers, every win %, and the colour of every result follows these settings.*

### Tags

#### Tags & Tag Groups

CONTROLS › TAGS & TAG GROUPS is the board where your tags live. A tag group holds tags of one kind, such as setups, mistakes, emotions or market conditions. Create tags and groups, drag a tag into a group or within it to reorder, drag a group by its name to reorder the groups, and double-click a name to rename it. Show the groups as cards side by side or as one stack.

A tag only appears in the journal and in the filters while it sits in a group. A new tag starts un-grouped until you drag it into one.

#### Exclusive Groups

Make a group exclusive and only one of its tags can be on a trade at a time: pick another and the first comes off. It suits anything that has a single answer, like the setup a trade was taken on or what the market was doing.

#### Trade and Day Tags

Each tag works on trades, on days, or both. A trade tag is set trade by trade in Trade & tagging. A day tag is set once in the debrief and counts for every trade of that day, so filters, splits and statistics can show your results on the days you slept badly, or the days with big news.

#### Signal Strength

Any tag can carry a number, positive or negative, with or without decimals. A trade's signal strength is the sum of its tags' numbers, its own and its day's. Score what makes a setup strong upwards and your warning signs downwards, and the journal shows whether your strongest trades really are your best ones: under a curve, a bar chart or a distribution, and as a column in your statistics and trade lists.

#### Retired Tags

A tag dragged out of every group is retired: hidden from the journal and from every filter, with the tag and its trades kept. Drag it back into a group and it is in use again, history and all. Deleting a tag for good removes it from every trade it was on, so retiring is the safe way to stop using one.

#### Starter Set and Other Journals

The STARTER SET gives you ready-made groups to start from: Setup, Mistakes, Mindset, Market, Hindsight and Day tags. You can also bring in the tags or the whole tag groups of your other journals. Nothing merges with what you have: a name already taken gets a number, like "Breakout (1)".

#### Calculate Stats

"CALCULATE STATS" in the Trade & tagging cell shows how the trades that carry the same tags as the picked trade have done: their count, win %, P&L, average trade, profit factor, drawdown and runup, beside the same for all trades. Light up the groups that should count, and narrow it with its own filters.

### Trades

#### Editing a Trade

Double-click any value in a trade list or on the trade card to change it. Right-click a trade and choose EDIT TRADE to edit every value at once, moving from one to the next with Tab. Enter or a click away keeps what you typed, Escape drops it.

What you type is kept over the trade's own values. The file you imported is never changed, the trade keeps its tags, rating, note and screenshots, a new import does not wipe your edits, and Reset edits brings the original values back. Change a price, the side or the size and the P&L is worked out again from the instrument's tick size and tick value.

*Note: An edited value is underlined with dots, so you can always tell a value you changed from one the file gave.*

#### Adding a Trade

"+ TRADE" adds a trade of your own to the day shown, opened straight into EDIT TRADE. Trades you add are kept in the journal, and only they can be deleted.

#### Merging Trades

Ctrl + click several trades of the same account, instrument and direction in Daily trades or the navigator's trade list, right-click them and choose Merge. They become one trade, and Unmerge splits them back. A trade made of several legs or merged trades carries a small mark of stacked rectangles, and hovering it lists the legs.

#### Ratings and Notes

Rate every trade from 1 to 3 for how well you traded it, whatever it paid, and write your note on it in the trade card. Click the same rating again to clear it. Ratings and notes are kept with the trade and travel in the exports, and ratings can split and filter every cell.

#### Commissions

Set a commission per contract, round turn, for every instrument or instrument group, then switch Commissions on in GLOBAL FILTERS. Every P&L in the journal then shows after commission, and the Comm column and statistic show what was paid.

### Screenshots

#### Adding Screenshots

Every trade holds as many screenshots as you like, and every prebrief and debrief holds strips of its own. Drop images onto the cell, paste one with Ctrl + V while the pointer is over it, or press IMPORT to pick files (PNG, JPG, GIF and WEBP). Drag a thumbnail to put it in another place, or have them put in the order they were taken.

#### The Viewer

Click a thumbnail to see the picture full size. Right-click it to edit, download or remove it, and Ctrl + click to pick several at once.

#### Screenshot Editor

"EDIT" opens the picture in the editor: arrows, lines, rectangles, ellipses, free drawing, text, and other pictures placed on top, such as a news release beside the chart. Every mark has its own colour, fill, outline, opacity and size, can be moved, copied, brought forward or sent back, and undo and redo cover every step. Rotate, crop and frame the picture itself.

The original picture is never changed. Your marks are kept beside it, so HIDE ALL shows the clean screenshot again at any time, and HIDE TEXT hides only the text.

#### Download

"DOWNLOAD" saves a copy of the screenshot with the marks shown drawn in, as a PNG, wherever you choose. The screenshot in the journal stays as it is.

### Recordings

#### YouTube Recordings

Stream or upload your trading session to YouTube, unlisted is fine with embedding allowed, and add its link in the Trade visualiser with the time on its first frame. From then on every trade the recording covers plays it from a few seconds before its entry, inside Records.

#### Local Recordings

Recordings on your computer work the same way. Drop the video files on the Trade visualiser or add them, and Records reads the start time from the file's name, as OBS writes it, or from the file itself. You can always edit the start time in place. A clip imported on one trade plays for that trade whatever its time, so short clips work as well as full sessions.

*Note: The common recording formats play: MP4, MKV and MOV with H.264, HEVC or AV1 video, as OBS records them by default.*

#### Before The Trade

"Before The Trade" sets how many seconds before the entry the recording starts, from 0 to 600, so you see the build-up and not only the fill. A button takes you to the exit as well.

#### Autoplay

With "Autoplay Video" on, a picked trade's recording plays by itself from its point. Off, it waits at that frame, paused. Only one player plays at a time.

#### Auto Screenshot

With "Auto Screenshot" on, every trade with a local recording gets its screenshots by itself, once. The whole session is taken as soon as the recording lands or any trade of that day is shown, from every local recording of that day, so you never click through the trades one by one. The points are yours to set in Auto Shots, as many as you like: ENTRY, MIDPOINT, EXIT and MODIFICATIONS, each with its own seconds before or after.

MODIFICATIONS takes one screenshot at every change of the position between the entry and the exit: each add and each partial exit. A trade that never changed size gets none.

Changing Auto Shots never touches screenshots already taken. It only reaches trades that have none yet. A screenshot you remove stays removed.

#### RE-TAKE and CLEAR

"RE-TAKE" takes a DAY or a TRADE again with the Auto Shots as they are now, from every local recording of that day. It adds a new batch and removes nothing, and each batch gets the next number in its name: auto2, auto3 and so on. "CLEAR" removes the auto screenshots of a DAY or a TRADE after asking you, and your imported screenshots stay. A cleared trade is not taken again by itself, so use RE-TAKE when you want new ones. STOP ends a run that is under way, and what it took stays.

*Note: Auto screenshots come from local recordings only. A YouTube recording gets none. The SCREENSHOT button on the player's bar takes a frame by hand, on both kinds of recording, and it lands in IMPORTED SCREENSHOTS.*

*Note: MODIFICATIONS needs a file that shows the position's changes, as Rithmic, MotiveWave, Topstep, Sierra Chart and grouped TradeCraft files do. For trades imported before version 1.2.0, import the same file again under the same name, then use RE-TAKE. RiskCells' own live logs write one line per trade, so those trades show none.*

### Controls

#### Journals

CONTROLS › JOURNALS lists every journal: OPEN loads one in this window, NEW WINDOW opens one beside it, and DUPLICATE, RENAME, EXPORT and DELETE do what they say. NEW JOURNAL starts a fresh, empty one. Keep a journal per account, per strategy or per year, and keep them apart for good.

#### Interface

Tooltips and Explanations switch the short notes under the pointer and the longer texts in the panels on and off. Zoom Window scales the whole window, Cell Bar Zoom the bars of the cells, Text Zoom the chart labels and tables, and Cell Bars can hide themselves until the pointer is over a cell. Magnet, Magnet Reach, Widget Padding, Show Ruler, Swap On Drop and Overlap set how cells snap and settle as you arrange them.

#### General Settings

Time Zone is the clock the journal shows every trade on: a city's local time with summer time, or the times exactly as written. Abbreviate writes headers and labels short (PF, Dur) or in full (Profit factor, Duration). Date Format writes dates day first or month first, everywhere in the journal.

#### Graphic Settings

GRAPHIC SETTINGS cover the font and its weight, hard or soft corners, the cell frames and cards, glow, blur, rim lights and edges, the chart grid, the zero line, gradients, axes, the crosshair, price lines, chart backgrounds per cell type, the canvas and its hex backdrop. CHART COLOURS set the colours of wins, losses and breakeven, of long and short, of MAE and MFE, of the three ratings and of an agent's highlight.

Save the look as a THEME under a name and apply it again with one click. LOAD THEME holds the premade DEFAULT and GLASS skins, and loads a theme file exported from RiskCells Trading, so Records and your trading windows can wear the same look.

#### Instruments

Every instrument arrives with its name exactly as the file writes it. Here it gets its tick size, tick value, commission per contract and colour. Right-click a column's header to give every instrument the same value.

Drag instruments into instrument groups, such as every MCL contract month, and charts, tables and filters count them as one. A group has its own colour, its own commission and its own breakeven range, and can override the commissions of its instruments.

#### Accounts

Every account found in your files is listed with its trades and where they came from. Give an account a display name, or hide it from every page.

#### Import and Export

IMPORT TRADES brings in your files: the journal they land in, the platform, Group Flat To Flat, the zone of their times, then CHOOSE FILES, CHOOSE FOLDER or a drop. IMPORTED FILES lists every import with its platform, trades, accounts and dates, its time zone, which you can still change, and a ✕ to remove it.

EXPORT writes the trades of a date range as a CSV, and EXPORT ALL (JSON) writes a journal's whole settings file, your journaling backup, which IMPORT (JSON) loads back. EXPORT TO A FOLDER writes real files you can open: Settings, Trades, Imported Files, Screenshots and Recordings, each with its own switch.

#### Agents MCP

AGENTS MCP connects the AI agent you use to your journal. SET UP YOUR AGENT copies the exact configuration for Claude Desktop, Claude Code, Codex, Cursor, VS Code or an agent in a container. Agent Access switches it all on and off. WHAT AGENTS MAY DO holds a switch for every kind of action, with the destructive ones off until you allow them, and Confirm In App asks you before any of those runs.

BACKUPS saves what a destructive task can change before it runs, ready to RESTORE. SCREENSHOTS AND REPORTS lets agents take pictures of your pages and cells for their reports. ACTIVITY lists every call an agent made, with its time, its tool and its result.

*Note: Agent Access is off until you switch it on. The server listens on your computer only and answers only calls that carry your install's token.*

#### Cloud Folder

CLOUD FOLDER keeps a copy of everything in a folder you choose, for example inside Dropbox, OneDrive or Google Drive, so another computer linked to it has the same journals, screenshots and recordings, up to date. Each computer keeps its own full copy and works from that, and only the changes travel. Nine switches under WHAT SYNCS choose what travels, for every computer on that folder.

"Sync Folder" pauses it. Your computer carries on from where it is, and changes made meanwhile keep the time they were made. When you turn it back on, both sides catch up, and nothing either side made is lost. A pause is not a split: what you did while it was off goes out too, deletes included.

#### Joining a Cloud Folder

The first time a computer that already holds data picks a folder in use, it shows both sides side by side and asks once. MERGE BOTH keeps everything from both. USE THE CLOUD FOLDER'S DATA makes the journals, pages, looks and settings the folder's. IGNORE changes nothing. Imported trades and screenshots are kept either way, and RiskCells saves a backup of that computer first, so if the backup cannot be saved, the computer does not join. An empty computer gets no question and just joins.

#### Confirm Changes For Sync

With "Confirm Changes For Sync" on, the first changes that reach a computer after it starts wait until you have seen them: what changed, on which computer, with both sides side by side. SYNC NOW brings them in. TURN SYNC OFF leaves the computer as it is, and the changes wait until you turn Sync Folder back on. After SYNC NOW that session syncs by itself. Switch it off and changes sync without asking. It is on by default, and each computer has its own.

#### Differences

"COMPARE" shows this computer's trades, newest trade and screenshots beside each of your other computers, at any time, also with Sync Folder off.

#### Big Delete

A delete nobody confirmed stops before it reaches your other computers, and RiskCells asks: KEEP THEM or DELETE EVERYWHERE. It stops at 5 or more things of a kind within 5 minutes, or when all of a kind go. Imported trades, trades added by hand and whole journals always stop, whatever the number, and so does an import that comes back with fewer trades. A delete you confirmed yourself passes.

#### Conflicts

Where two computers changed the same thing, the later change wins and the other is kept under CONFLICTS, ready to RESTORE.

*Note: Your sign-in, the agents' token and the Stream Deck token never travel. They stay on each computer.*

*Note: Windows stay where each computer has them, so five monitors on one computer and one on the other is fine. Window places only travel between computers whose screens are laid out exactly the same.*

*Note: RiskCells Trading's settings travel too, with their own switch, and apply at the other computer's next start. Confirm Changes For Sync and Big Delete are for Records.*

#### Backup

"BACKUP NOW" saves every journal, the imports, the screenshots and Trading's settings in one file, in a folder you choose, under a name you give it. RESTORE brings it back as new journals with FROM BACKUP in their names, so nothing you have is replaced. RiskCells never changes or deletes a backup. An agent can add one when you ask it to, but it can never replace or delete one.

*Note: Recordings stay where they are, so keep your own copy of those files. EXPORT TO A FOLDER can copy them.*

#### About

ABOUT is the same as in RiskCells Trading: your licence, account, billing and devices, the version and its updates, and usage data. Change something on either side and the other shows it at once.
