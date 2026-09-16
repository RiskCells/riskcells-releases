[← Back to RiskCells](readme.md)

# TradingView

## BEFORE YOU START: THE TRADINGVIEW BRIDGE IS A BETA

RiskCells connects to TradingView through a browser extension called RiskCells TV Bridge
(BETA). The extension reads the values you choose on your TradingView charts and passes
them to a small RiskCells helper on your PC, which writes them as feeds for RiskCells.

Please read this first:
- This is a beta version. It is still being tested, so things can change and you may run
  into problems. Please tell us when you do (see the end of this guide).
- It is not in the Chrome Web Store. You add it to your browser yourself, from a
  folder, with the browser's Developer mode switched on (Part 4). Your browser may warn
  you about extensions in developer mode, and Microsoft Edge shows a notice about them.
  That is expected for the beta: keep the extension switched on.
- It does not update by itself. When a new version comes out, you replace it yourself
  (see UPDATING THE BRIDGE).
- It is made by RiskCells, not by TradingView. It reads your charts on the TradingView
  website, and TradingView can change its website at any time. A change like that can
  stop the bridge until we release an update. When the bridge can't read a chart, its
  panel shows a warning.
- It works with charts on tradingview.com in Google Chrome, Microsoft Edge and Vivaldi.
  It does not work in the TradingView desktop app, or with TradingView charts inside
  other websites, such as a broker's platform.
- The bridge sends nothing over the internet. It only passes your chart values to the
  helper on your PC.
- You need RiskCells 1.1.1 or later, which includes the helper.

## PART 1: INSTALL RISKCELLS

1. Download RiskCells. Use the download link in your welcome email, or go to riskcells.com,
   open Resources and choose Download Software. The file is called RiskCells-Setup.exe.

2. Double-click RiskCells-Setup.exe.
   - If Windows shows "Windows protected your PC", click More info, then Run anyway.
   - If Windows asks for permission to make changes, click Yes.

3. Follow the installer.

4. Open RiskCells from the desktop shortcut or the Start menu.

5. Leave RiskCells open for at least 30 seconds the first time. In that time it registers
   its TradingView helper with Chrome and Edge, so the extension can find the helper. If
   you use a version older than 1.1.1, download and install the latest version first.

## PART 2: SIGN IN

1. Enter the email address you used at checkout and click SIGN IN.

2. We email you a 6-digit code. Type it in. You are signed in as soon as you enter the
   last digit.
   - No email? Check your spam folder, or click RESEND CODE.
   - Typed the wrong address? Click DIFFERENT EMAIL.

This computer now stays signed in, so later starts need no code. If every device on your
plan is already in use, the sign-in screen lists them so you can release one. Releasing a
device sends a new one-time code to your email, so only the account holder can manage
devices.

The first time you sign in, the FEATURES window opens together with your RiskCells window.
Click through it to get to know the main settings and features. You can close it and
reopen it any time from the Window Picker in the main control bar, where it is listed as
FEATURES.

## PART 3: CONNECTING YOUR PLATFORM: TRADINGVIEW

1. On riskcells.com, open Resources and choose Download TradingView Bundle. The file is
   called RiskCells-TradingView-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside is a folder called
   RiskCells-TV-Bridge with the extension's files, including manifest.json.

3. Move the RiskCells-TV-Bridge folder to a place where it can stay, for example your
   Documents folder. Your browser runs the extension from this folder, so don't delete,
   move or rename it after Part 4.

## PART 4: ADD THE EXTENSION TO YOUR BROWSER

The bridge is not in the Chrome Web Store, so you add it with your browser's Developer
mode. Use the browser you open TradingView in.

### GOOGLE CHROME

1. Type chrome://extensions in the address bar and press Enter.

2. Switch on Developer mode.

3. Click Load unpacked.

4. Choose the RiskCells-TV-Bridge folder, the one with manifest.json directly inside it,
   and click Select Folder. RiskCells TV Bridge (BETA) now shows on the page.

5. Pin it to the toolbar: click the Extensions button next to the address bar, then click
   the pin next to RiskCells TV Bridge (BETA).

### MICROSOFT EDGE

1. Click Settings and more (...), then Extensions, then Manage extensions.

2. Switch on Developer mode.

3. Click Load unpacked, choose the RiskCells-TV-Bridge folder and click Select Folder.

4. Click the Extensions button next to the address bar, then click RiskCells TV Bridge
   (BETA). Its icon is added next to the address bar.

### VIVALDI

Follow steps 1 to 4 for Google Chrome, but type vivaldi://extensions in step 1.

From now on your browser may warn you about extensions in developer mode, for example when
it starts. Keep RiskCells TV Bridge switched on.

## PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

RiskCells reads its feeds from a folder on your PC. Create one folder for all your feeds
first, then let the bridge write into it.

1. Create the folder: in File Explorer, open This PC, then your C: drive. Right-click an
   empty area, choose New > Folder and name it RiskCells Feeds. Don't use a folder that
   OneDrive or Dropbox syncs, because the feed files change many times a second. If you
   already have a feed folder for another platform, use that one instead.

2. In your main RiskCells window, open Master Settings, then Risk Parameters.

3. Near the bottom of Risk Parameters, click the folder icon next to Feed Folders.

4. Click + Add Folder and choose your feed folder, for example C:\RiskCells Feeds.

RiskCells picks up a new folder within a few seconds. Now set the same folder in the
bridge:

5. Click the RiskCells TV Bridge icon in your browser's toolbar. The TV Bridge panel opens.

6. At the top of the panel, check that it says STATUS: LIVE. If it says STATUS: STALE, see
   TROUBLESHOOTING.

7. At the bottom of the panel, replace the text in the FEED FOLDER box with the full path
   of your feed folder, for example C:\RiskCells Feeds. To copy the path, open the folder
   in File Explorer, click the address bar and press Ctrl + C, then paste it into the box.

8. Click Apply next to the box. It shows CONFIRMED when the helper has accepted the
   folder. Until you change it, the bridge writes to C:\Users\Public\Documents.

## PART 6: CONNECT YOUR TRADINGVIEW CHARTS

How to connect a feed. Do this for each feed you want to send to RiskCells:

- A. Open your chart on tradingview.com/chart, in the browser you added the extension to.
- B. Click the RiskCells TV Bridge icon in the toolbar. The panel lists your TradingView tabs and the charts in them, each with its symbol, its interval and the feed it makes, such as hourly feed or daily feed. Under each chart is a Mouse row and a row for each indicator on that chart.
- C. In the row, type a name in the name box and press Enter. RiskCells shows the feed under exactly this name.
- D. Click the switch at the start of the row.
- E. After a moment, the row shows writing and a number that keeps going up. The feed is now being written.

Tips:
- The panel closes when you click somewhere else. To keep it open while you set up, click
  Open as window at the top of the panel.
- Names: don't add .json, and don't use \ / : \* ? " \< > \|. A name can have up to 64
  characters and can't start with atr\_, realtime\_, ACCLIVE\_ or DTDSLIVE\_.
- Every ATR feed needs its own name, and an ATR feed can't use the same name as a Mouse
  feed.

### MOUSE TICKS

1. Open a chart of the instrument you trade. Any interval works.

2. In the panel, find the Mouse row under that chart. It is always the first row. Name it,
   for example ES MOUSE, and switch it on (steps C to E above).
   There are no settings. The bridge measures the distance from the last price (the close
   of the current bar) to your mouse pointer, in the symbol's tick size on TradingView,
   and sends it in whole ticks.

3. In RiskCells, choose this feed in the dropdown of the field you want it to drive. Most
   often that is Stop / Ticks. Then move your mouse pointer over the chart: Stop / Ticks
   follows the distance in ticks from the price to your pointer, and Contracts is
   recalculated from it straight away.

   Note: when a calculator's ATR field has a value, RiskCells works out Stop / Ticks from
   the ATR instead, and the Mouse Ticks value is replaced. On the calculator you use for
   Mouse Ticks, turn ATR off with its ATR button.

Good to know:
- The feed file is created the first time you move your mouse over the chart after you
  switch the row on. Until then, the row says move the mouse over the chart.
- Using several charts? Give the Mouse row on each chart the same name. Only the chart
  under your mouse sends its value, and the other charts show standby. When you move to
  another chart, it takes over about 4 seconds after you leave the previous chart.

### HOURLY ATR

1. Open a chart of the instrument and set its interval to 1 hour: choose it in the
   interval menu in the toolbar at the top of the chart, or click the chart, type 60 and
   press Enter. Don't use the date range buttons below the chart, such as 1D: they change
   the interval too (1D shows one day of 1-minute bars). In the panel, the chart now shows
   hourly feed.

2. Add TradingView's Average True Range indicator: click Indicators in the toolbar at the
   top of the chart, type Average True Range and click it in the list. In the indicator's
   settings, set Length and the smoothing to match the ATR you normally use. TradingView's
   default is Length 14 with RMA smoothing.<br>
   Note: you don't have to use ATR. ATR is the name of the button in RiskCells that shows
   these fields, but RiskCells does not care what the value is based on. You can switch on
   the row of any other indicator on the chart that draws a line. RiskCells uses its value
   like an ATR, as a distance in price, so an indicator that shows a price level or a
   score, such as a moving average or RSI, gives wrong stops. If the indicator draws
   several lines, the bridge sends the first one. Values below zero are not sent:
   RiskCells keeps showing the last value from before it went below zero, and its dot
   stays blue.

3. In the panel, the chart's ATR row comes right after the Mouse row. Name it, for example
   ES 1H, and switch it on (steps C to E above).

4. In RiskCells, choose the feed (for example ES 1H) in the dropdown above the ATR field.
   DYN turns on by itself and the ATR field fills (see ATR MODES below). If a calculator
   shows no ATR field, turn ATR on with its ATR button first.

Tip: leave the contract month out of the name and add the timeframe instead, so the feed
is easy to find later, for example ES 1H.

Good to know:
- The hour labels follow your chart's time zone setting on TradingView.
- The trading day follows the symbol's trading session on TradingView, so there is
  nothing to set.
- On a chart below 1 hour, the feed keeps one reading per hour (the last completed bar of
  that hour), and the ATR is the ATR of those shorter bars. Use a 1-hour chart for the
  hourly ATR.
- The feed belongs to the chart, not to the symbol. If you change the chart's symbol or
  interval, the same feed sends the new values under the same name.

### DAILY ATR

1. Open a chart of the instrument and set its interval to 1 day: choose it in the interval
   menu at the top of the chart, or click the chart, type 1D and press Enter. In the panel,
   the chart now shows daily feed. If your TradingView plan allows only one chart per
   layout, open this chart in its own browser tab.

2. Add the Average True Range indicator (or the indicator you want to use) to this chart,
   as for the hourly ATR.

3. In the panel, name this chart's ATR row, for example ES 1D, and switch it on (steps C to
   E above). The feed sends today's ATR, today's highest ATR so far and the last 5
   completed days. LOCK picks from these days.

4. In RiskCells, choose ES 1D in the dropdown above the ATR field. DYN turns on by itself.

### ACCOUNT VALUES

The bridge sends chart values and your mouse position only. It does not send account
values such as your balance, so there is no Account Link for TradingView. The live risk
modes in Risk Parameters (DTDS Live, ACC % Live and KELLY Live) need an account feed, so
with TradingView alone you set your risk on the calculators yourself.

### ATR MODES: DYN, MAX AND LOCK

When you choose an ATR feed, DYN, MAX and LOCK appear on the calculator, and DYN turns on
by itself (unless LOCK is already on), so the ATR field fills straight away.

- DYN follows the live ATR and keeps updating.
- LOCK holds one past reading that you pick in the list next to it.<br>
  Hourly feed: pick a time of day (Latest = the last completed hour). If that time has not
  come yet today, yesterday's reading at that time is used.<br>
  Daily feed: pick a day of the week (Previous = the last completed day).
- MAX works together with DYN or LOCK and uses today's highest ATR so far. On an hourly
  feed with LOCK, MAX uses today's highest ATR until your chosen time comes, then the
  reading at that time.

Click DYN or LOCK to switch between them. While a feed is chosen, one of the two is always
on, so clicking the one that is already on changes nothing. To stop using the feed, choose
MANUAL in the dropdown. While ATR is in use, RiskCells sets Stop / Ticks from the ATR and
the percentage button you choose on the calculator.

### SAVE YOUR LAYOUT

- Save your TradingView layout with Ctrl + S, or switch on Autosave in the layout menu.
- The bridge remembers your feeds in your browser. After you restart the browser, open the
  same charts again: each feed reconnects by itself to a chart that shows the same symbol
  in the same place of the same layout.
- A feed whose chart is not open is listed under Remembered feeds not on screen. It
  continues by itself when that chart is open again. You can also drag it onto a chart in
  the panel, or click Apply when a chart with the same symbol is open. Forget removes it.

### UPDATING THE BRIDGE

The bridge does not update by itself. When a new version comes out:

1. Download RiskCells-TradingView-Bundle.zip again and extract it (Part 3).

2. Replace your RiskCells-TV-Bridge folder with the new one, in the same place.

3. Open your browser's extensions page (Part 4) and reload RiskCells TV Bridge (BETA): in
   Chrome and Vivaldi, click the reload arrow on its card. In Edge, click Reload on its
   card.

4. Reload your TradingView chart tabs with F5.

Your feeds and your FEED FOLDER stay as they are.

## PART 7: SMOOTHER UPDATES (OPTIONAL)

The bridge sends Mouse Ticks up to 20 times a second (every 50 ms), and RiskCells reads
Stop / Ticks and ATR feeds every 100 ms by default. For a smoother Stop / Ticks value you
can make RiskCells read faster. Faster reading uses more CPU, so read the warning below
first.

The bridge's speed is fixed, so there is nothing to change in the bridge. ATR changes
slowly, so your ATR feeds can stay as they are.

In RiskCells, in your main window:

1. Open Master Settings > Risk Parameters. At the bottom you can set how often RiskCells
   reads each type of feed, in milliseconds (10 to 5000):
   - ATR Poll ms (default 100): ATR feeds
   - Stop Ticks ms (default 100): Stop / Ticks and Contracts feeds
   - Live R ms (default 1000): feeds chosen for R, and the live feeds in Risk Parameters
   - Monitor Widget ms (default 1000): the values in your Monitor Cells

   For smoother Mouse Ticks, set Stop Ticks ms to 50.

2. Click Restart now when RiskCells asks. The new rates apply to all windows after the
   restart.

### WARNING

- Very fast poll rates make RiskCells work harder, especially with many feeds and windows
  open.
- If RiskCells or your PC starts to lag, raise the numbers again, for example to 100.

## PART 8: CHECK THAT EVERYTHING WORKS

- The TV Bridge panel says STATUS: LIVE.
- Every row you switched on shows writing, and its number keeps going up. When several
  charts share one Mouse name, the charts you are not pointing at show standby.
- The bridge's toolbar icon shows the number of feeds being written, on a blue badge.
- In RiskCells, the dots beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in the calculator's ATR field.

### HOW TO READ THE LIVE / STALE INDICATORS

In the TV Bridge panel:
- STATUS: LIVE (blue): the bridge is connected to the RiskCells helper.
- STATUS: STALE (pink): the bridge can't reach the helper. It keeps trying by itself. Click
  STATUS: STALE to try again straight away.
- The badge on the toolbar icon: a blue number is the number of feeds being written. A
  pink ! means the helper is not connected. A yellow ! means a feed has a problem and none
  are being written.

In RiskCells, every feed has a coloured dot. Each feed dropdown on a calculator has its own
dot, and each row has a master dot next to the row name.

Feed dot:
- Blue: the feed is updating.
- Pink: no update for about 8 seconds, or the feed has no usable value. The last value
  stays in the field.
- Grey: MANUAL, no feed selected.

Master dot, for all the feeds selected in that row:
- Blue: every selected feed is updating. It is also blue when no feed is selected.
- Yellow: at least one feed has stopped while others are updating. Look for the pink dot in
  that row.
- Pink: none of the selected feeds are updating.

These are the default colours. You can change them in Master Settings > Graphic Settings.

## TROUBLESHOOTING

**The extension does not load**
- The browser says the manifest file is missing: you chose the wrong folder. Choose the
  RiskCells-TV-Bridge folder, the one with manifest.json directly inside it.
- Extract the zip file first. The browser can't load the extension from inside the zip.
- Load unpacked only shows once Developer mode is switched on.

**The panel says STATUS: STALE, or a row says helper not connected**
- Make sure RiskCells 1.1.1 or later is installed. Start RiskCells, leave it open for at
  least 30 seconds, then click STATUS: STALE.
- Point at STATUS: STALE with your mouse to see the browser's reason.
- Vivaldi uses the same helper registration as Chrome, so these steps apply there too.

**The panel says No TradingView chart tab connected**
- Open your chart on tradingview.com/chart in the same browser.
- If the chart was already open before you added the extension, click Rescan tabs, or
  reload the chart tab with F5.
- A warning under the tab's name means the bridge can't read that page. Reload the tab. If
  the warning stays, TradingView may have changed its website. Please tell us (see the
  end of this guide).

**The ATR row is missing, or a row says not selectable**
- Add TradingView's Average True Range indicator to that chart and wait until it has
  loaded.
- If the chart shows tick size unknown in the panel, the bridge can't turn this symbol's
  prices into ticks, so it can't send feeds for it.

**A row shows a message instead of writing**
- give the feed a name first: type a name, press Enter, then switch the row on.
- name owned by tab (and a number): another browser tab is writing a feed with this name.
  Pick another name, or switch that feed off.
- is already used by: another feed in the panel has this name. Pick another name, or
  switch that feed off.
- already streaming from another tab: this chart is already sending its feed from another
  tab. The first tab keeps it.
- waiting for chart history: the chart is still loading its bars. Wait a moment.
- ATR has no value on the current bar yet: wait until the indicator shows a value.

**A feed is missing from the RiskCells dropdown**
- Check that its row in the panel shows writing.
- Check that the FEED FOLDER in the panel is your feed folder, and that this folder is
  listed in Feed Folders and switched on. Until you change FEED FOLDER, the bridge writes
  to C:\Users\Public\Documents.
- Look for the exact name you typed in the row.

**Apply next to FEED FOLDER shows REJECTED or NOT WRITABLE**
- folder does not exist: the path has a typo, or the folder was not created yet. The
  bridge does not create folders. Copy the exact path from the address bar of your feed
  folder in File Explorer and paste it into the box.
- folder is not writable, or NOT WRITABLE: choose a folder you can save files in, such as
  the folder you created in Part 5.
- helper not connected: fix STATUS: STALE first (see above). The bridge sends the folder
  to the helper when it reconnects.

**Stop / Ticks does not follow my mouse**
- Check that the chart's Mouse row is switched on and shows writing while you move your
  mouse over the chart.
- Move your mouse over the price area of the chart.
- If the calculator's ATR field has a value, Stop / Ticks is worked out from the ATR
  instead. Turn ATR off on that calculator with its ATR button.
- Using the same Mouse name on several charts? The chart you point at takes over about 4
  seconds after you leave the previous chart.
- no crosshair events on this chart: the bridge can't follow your mouse on this chart.
  Reload the tab. If it stays, please tell us (see the end of this guide).

**A feed dot is pink**
- RiskCells has had no update from the bridge for about 8 seconds. Check that the
  TradingView tab is still open, its row still shows writing, and the panel says STATUS:
  LIVE. Closing a TradingView tab stops its feeds.

**ATR shows 0 or looks wrong**
- Check the chart's interval: 1 hour for the hourly ATR, 1 day for the daily ATR.
- Check that Length and the smoothing match the ATR you normally use.
- The feed follows the chart: if you changed the chart's symbol or interval, the feed now
  sends that chart's values.

Need help? Click the version number next to TV BRIDGE (BETA) at the top of the panel. This
copies a status report. Paste it into an email to info@riskcells.com and tell us what
happened.
