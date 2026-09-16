[← Back to RiskCells](readme.md)

# NinjaTrader

## PART 1: INSTALL RISKCELLS

1. Download RiskCells. Use the download link in your welcome email, or go to riskcells.com,
   open Resources and choose Download Software. The file is called RiskCells-Setup.exe.

2. Double-click RiskCells-Setup.exe.
   - If Windows shows "Windows protected your PC", click More info, then Run anyway.
   - If Windows asks for permission to make changes, click Yes.

3. Follow the installer.

4. Open RiskCells from the desktop shortcut or the Start menu.

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

## PART 3: CONNECTING YOUR PLATFORM: NINJATRADER

1. On riskcells.com, open Resources and choose Download NinjaTrader Bundle. The file is
   called RiskCells-NinjaTrader-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside are four zip files, one for each
   indicator. Do not unzip these four: NinjaTrader imports them as zip files.
   - RiskCellsTicksFromMouseV5_NT.zip   (Mouse Ticks)
   - RiskCellsAtrFeed_NT.zip            (Hourly ATR)
   - RiskCellsAtrFeedDaily_NT.zip       (Daily ATR)
   - RiskCellsAccountLink_NT.zip        (Account Link)

## PART 4: IMPORT THE INDICATORS INTO NINJATRADER

1. In the NinjaTrader Control Center, go to Tools > Import > NinjaScript Add-On.

2. Select RiskCellsTicksFromMouseV5_NT.zip and click Import. NinjaTrader tells you when the
   import is complete.

3. Repeat for the other three zip files.

## PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

RiskCells reads its feeds from a folder on your PC. Create one folder for all your
indicators first, so they all write to the same place.

1. Create the folder: in File Explorer, open This PC, then your C: drive. Right-click an
   empty area, choose New > Folder and name it RiskCells Feeds. Don't use a folder that
   OneDrive or Dropbox syncs, because the feed files change many times a second. If you
   already have a feed folder for another platform, use that one instead.

2. In your main RiskCells window, open Master Settings, then Risk Parameters.

3. Near the bottom of Risk Parameters, click the folder icon next to Feed Folders.

4. Click + Add Folder and choose your feed folder, for example C:\RiskCells Feeds.

5. In Part 6, enter this same folder as the Output folder path in every RiskCells
   indicator. One folder for all your feeds is easier to maintain, and RiskCells has only
   one folder to watch.

RiskCells picks up a new folder within a few seconds.

## PART 6: ADD THE INDICATORS TO YOUR CHARTS

How to add a RiskCells indicator to a chart. Do this for each indicator, on every chart you
want to send data to RiskCells from:

- A. Click on the chart and press Ctrl + I, or right-click the chart background and choose Indicators.
- B. Type RiskCells in the Search box.
- C. Double-click the indicator in the Available list. It now appears in the Configured list.
- D. Select it in the Configured list. Its settings are in the Properties section on the right.
- E. When the settings are done, click OK.

This is how the indicators are named in the Available list:

| Indicator | Name in the list |
|---|---|
| Mouse Ticks | RiskCells™ MouseTicksControl v5 |
| Hourly ATR | RiskCells™ ATR FEED |
| Daily ATR | RiskCells™ ATR FEED DAILY |
| Account Link | RiskCells™ ACCOUNT LINK |

### MOUSE TICKS

1. Open a chart of the instrument you trade. Any timeframe works.

2. Add RiskCells™ MouseTicksControl v5 (steps A to E above). Its settings, in the order you
   see them:

   - Current Price Source (default: Bid)<br>
     The live price the distance is measured from: Bid, Ask or Last Trade.

   - Study Update Delay in Milliseconds (default: 0)<br>
     The shortest time between two readings of your mouse position. 0 reads every mouse
     movement, which is the fastest. A higher number uses less CPU but updates less often.

   - Chart Compression Factor (default: 1)<br>
     Made for compressed charts and DOMs on instruments with big ranges, such as NQ. The
     indicator measures the distance in the instrument's ticks and divides it by this
     number. Leave it at 1 so RiskCells gets the real tick count your risk is calculated
     from. If you use another number, set the tick value in RiskCells to match the bigger
     step.

   - Round Output (default: ticked)<br>
     Ticked sends whole ticks. Unticked sends the exact value with two decimals.

   - JSON Name (default: CUSTOM NAME)<br>
     The name of this feed in RiskCells, for example ES TICKS. Use letters, numbers and
     spaces only.

   - JSON Write Interval in Milliseconds (default: 100)<br>
     The shortest time between two updates of the feed file. 0 writes as fast as
     practical, about every 25 ms. Lower is smoother but uses more CPU (see Part 7).

   - Output folder path (default: empty)<br>
     The folder the feed file is written to. Enter your feed folder from Part 5, for
     example C:\RiskCells Feeds.

   - Multi-Chart Mouse Handoff (default: ticked)<br>
     Made so one feed can follow your mouse across several charts. Ticked: when charts
     share the same JSON Name, only the chart under your mouse sends its value. Unticked:
     this chart always sends, so only untick it when each chart has its own JSON Name.

   - Show readout on chart (default: ticked)<br>
     Shows the distance on the chart, for example "12 ticks".

   - Readout corner (default: TopRight)<br>
     The corner of the chart where the readout sits.

3. In RiskCells, choose this feed in the dropdown of the field you want it to drive. Most
   often that is Stop / Ticks. Then move your mouse pointer over the chart with the
   indicator: Stop / Ticks follows the distance in ticks from the price to your pointer, and
   Contracts is recalculated from it straight away. The readout shows the same distance on
   the chart.

   Note: when a calculator's ATR field has a value, RiskCells works out Stop / Ticks from
   the ATR instead, and the Mouse Ticks value is replaced. On the calculator you use for
   Mouse Ticks, turn ATR off with its ATR button.

Good to know:
- The feed file is created the first time you move your mouse over the chart, as long as
  NinjaTrader is connected and receiving live prices.
- Only the price panel of the chart counts. Moving over a panel below it is ignored.
- The readout on the chart updates up to 4 times a second, because that is how often
  NinjaTrader redraws charts. RiskCells reads the feed file directly, so it is not slowed
  down by this.
- Using several charts? Add the indicator to each chart with the same JSON Name. Only the
  chart under your mouse sends its value, so RiskCells follows the chart you point at.

### HOURLY ATR

1. Open a 1-hour chart of the instrument: right-click the chart background, choose Data
   Series, set Type to Minute and Value to 60, then click OK.

2. Add RiskCells™ ATR FEED (steps A to E above). In its Properties, set:
   - Input series: click the field and choose ATR under Indicators, with the Period you use
     (14 by default). This is the ATR RiskCells receives. Until it is set, the indicator
     writes nothing.
   - Instrument name: the name RiskCells shows for this feed, for example ES 1H. If you
     leave it empty, it uses the chart's symbol, for example ES.
   - Output folder path: enter your feed folder from Part 5.
   - JSON Write Interval in Milliseconds (default: 250): how often the feed file is updated.

   Click OK.

3. In RiskCells, choose the feed (for example ES 1H) in the dropdown above the ATR field. DYN turns on by itself and the ATR field fills (see ATR MODES below).

Tip: leave the contract month out of the name and add the timeframe instead, so the feed
is easy to find later, for example ES 1H.

### DAILY ATR

1. Open a daily chart of the instrument: in Data Series, set Type to Day and Value to 1,
   then click OK.

2. Add RiskCells™ ATR FEED DAILY (steps A to E above). In its Properties, set:
   - Input series: ATR under Indicators, the same way as for the hourly chart.
   - Instrument base name: for example ES. The indicator adds -D1 for the daily timeframe,
     so the feed shows as ES-D1. If you leave it empty, it uses the chart's symbol.
   - Output folder path: enter your feed folder from Part 5.
   - JSON Write Interval in Milliseconds (default: 250): how often the feed file is updated.

   Click OK.

3. In RiskCells, choose ES-D1 in the dropdown above the ATR field. DYN turns on by itself and the ATR field fills (see ATR MODES below).

### ACCOUNT LINK

Account Link sends your NinjaTrader account values, such as your balance, to RiskCells. The
live risk modes in Risk Parameters use them to size from your real balance, and Monitor
Cells can show them.

1. To see what your broker sends, open the NinjaScript Output window first: in the Control
   Center, go to New > NinjaScript Output.

2. Open any chart. Account Link needs a chart to run on, but the instrument does not matter.

3. Add RiskCells™ ACCOUNT LINK (steps A to E above). Its settings, in the order you see
   them:

   - Output folder path (default: empty)<br>
     Enter your feed folder from Part 5.

   - JSON Write Interval in Milliseconds (default: 250)<br>
     How often the account feeds are updated. 0 writes as fast as practical.

   - File name prefix (default: empty)<br>
     Empty names each feed after its account, for example Sim101. With a prefix, the name
     becomes the prefix followed by the account name.

   - Print field dump to Output window (default: ticked)<br>
     Lists every value your broker sends for each account, once, in the NinjaScript Output
     window. Values depend on your broker, so this shows which ones you actually get.

   Account Link writes one feed for each account NinjaTrader lists. Only one copy writes to
   a folder, so adding it to more charts changes nothing.

4. In RiskCells, open Master Settings > Risk Parameters and click the live mode you use:
   DTDS Live, ACC % Live or KELLY Live. Fill in its settings, choose your account in its
   Feed dropdown, then choose the value to size from in the list next to it, for example
   Net Liquidation.<br>
   Note: until you choose a value, RiskCells uses the first one in alphabetical order. On
   NinjaTrader that is usually Buying Power, which is often 0.

5. On each calculator that should use it, choose the same account in the dropdown above
   Risk. Risk per trade then comes from the live mode.<br>
   Note: if that account is not the Feed of the live mode that is on, Risk takes the plain
   value chosen next to the dropdown instead, for example your whole balance.

6. To show an account value in a Monitor Cell, right-click a Monitor button and choose the
   account, then the value.

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

### SAVE YOUR WORKSPACE

When your indicators are in place, save your workspace from the Workspaces menu in the
Control Center, so they are there the next time you open NinjaTrader. NinjaTrader also asks
whether to save when you close it.

## PART 7: SMOOTHER UPDATES (OPTIONAL)

The Mouse Ticks indicator writes its feed every 100 ms, and RiskCells reads Stop / Ticks and
ATR feeds every 100 ms by default. For a smoother Stop / Ticks value you can make both
faster. Faster updates use more CPU, so read the warning below first.

In NinjaTrader, on each chart that has the Mouse Ticks indicator:

1. Open the indicator's settings (Ctrl + I, then select it in the Configured list). Set
   "JSON Write Interval in Milliseconds" to 0, so it writes as fast as practical (about
   every 25 ms). Keep "Study Update Delay in Milliseconds" at 0. Click OK.

The indicator writes on its own timer, so there is no NinjaTrader chart setting to change.
The readout on the chart stays at up to 4 updates a second. ATR changes slowly, so your ATR
indicators can stay as they are.

In RiskCells, in your main window:

2. Open Master Settings > Risk Parameters. At the bottom you can set how often RiskCells
   reads each type of feed, in milliseconds (10 to 5000):
   - ATR Poll ms (default 100): ATR feeds
   - Stop Ticks ms (default 100): Stop / Ticks and Contracts feeds
   - Live R ms (default 1000): feeds chosen for R, and the live feeds in Risk Parameters
   - Monitor Widget ms (default 1000): the values in your Monitor Cells

   For smoother Mouse Ticks, set Stop Ticks ms to 50.

3. Click Restart now when RiskCells asks. The new rates apply to all windows after the
   restart.

### WARNING

- Faster updates cost CPU in both NinjaTrader and RiskCells.
- Very fast poll rates also make RiskCells work harder, especially with many feeds and
  windows open.
- If NinjaTrader or your PC starts to lag, raise the numbers again, for example to 100.

## PART 8: CHECK THAT EVERYTHING WORKS

- The readout on your NinjaTrader chart changes as you move the mouse.
- In RiskCells, the dots beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in the calculator's ATR field.
- Your account value shows in the live mode in Risk Parameters.

### HOW TO READ THE LIVE / STALE INDICATORS

RiskCells shows the state of every feed with a coloured dot. Each feed dropdown on a
calculator has its own dot, and each row has a master dot next to the row name.

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

**The indicators are not in the Indicators window**
- Import each of the four zip files as they are, without unzipping them (Tools > Import >
  NinjaScript Add-On).
- If NinjaTrader says other NinjaScript files on your PC have programming errors, those
  errors must be fixed, or those files removed, before you can import. NinjaTrader compiles
  all custom NinjaScript together.
- Type RiskCells in the Search box of the Indicators window.

**A feed is missing from the RiskCells dropdown**
- Mouse Ticks: move your mouse over the chart's price panel. The file is created on the
  first movement, and NinjaTrader must be connected and receiving live prices.
- Hourly and Daily ATR: check that Input series is set to ATR. Until it is set, the
  indicator writes nothing.
- Account Link: make sure NinjaTrader is connected, so your account is available.
- Check that the folder in the indicator's Output folder path is listed in Feed Folders and
  switched on.
- A typo in the Output folder path does not show an error: the indicator creates a new
  folder with the mistyped name and writes the feed there, where RiskCells does not look.
  Copy the exact path from the address bar of your feed folder in File Explorer and paste
  it into the setting.
- Look for the name you gave the indicator: its JSON Name, its Instrument name (or the
  chart's symbol), its base name with -D1 added (Daily ATR), or the account name (Account
  Link).

**Stop / Ticks does not follow my mouse**
- Move your mouse over the price panel of the chart that has the indicator.
- If the calculator's ATR field has a value, Stop / Ticks is worked out from the ATR
  instead. Turn ATR off on that calculator with its ATR button.
- Using the same JSON Name on several charts and you closed the chart that was sending?
  Move your mouse over another chart with that name. It takes over within a few seconds.

**A feed dot is pink**
- RiskCells has had no update from that indicator for about 8 seconds. Check that
  NinjaTrader is open and connected, and the indicator is still on the chart.
- For an ATR feed, check that DYN or LOCK is on.

**ATR shows 0**
- Check that DYN or LOCK is on.
- Open the ATR indicator's settings and check that Input series is set to ATR.

**Account value shows 0**
- In Risk Parameters, choose the value in the list next to the live mode's Feed dropdown.
  Until you do, RiskCells uses the first value alphabetically, usually Buying Power.
- Values depend on your broker. Tick Print field dump to Output window to see which values
  your connection sends.

Need help? Email info@riskcells.com.
