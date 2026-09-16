[← Back to RiskCells](readme.md)

# Sierra Chart

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

## PART 3: CONNECTING YOUR PLATFORM: SIERRA CHART

1. On riskcells.com, open Resources and choose Download Sierra Chart Bundle. The file is
   called RiskCells-SierraChart-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside are three files:
   - RiskCellsTicksFromMouse_SC.dll   (Mouse Ticks)
   - RiskCellsAtrFeed_SC.dll          (Hourly ATR)
   - RiskCellsAtrFeedDaily_SC.dll     (Daily ATR)

## PART 4: COPY THE STUDIES INTO SIERRA CHART

1. Open the file path where your Sierra Chart is installed and navigate to the "Data" folder.
   Usually the path is: C:\SierraChart\Data

2. Copy the three DLL files into that folder.

3. Running more than one Sierra Chart instance? Copy the files into the Data folder of your
   main instance, then restart Sierra Chart so the studies appear in your other instances.

## PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

RiskCells reads its feeds from the folders you give it. Set this up first, so you can point
every study at the same folder in Part 6.

1. In your main RiskCells window, open Master Settings, then Risk Parameters.

2. Near the bottom of Risk Parameters, click the folder icon next to Feed Folders.

3. A new install already lists C:\SierraChart\Data. Leave it switched on.
   If it is not in the list, or Sierra Chart is installed somewhere else, click + Add
   Folder and choose your Sierra Chart Data folder. We suggest this folder because it is
   where Sierra Chart keeps its data anyway.

4. Use this same folder as the Output folder path in every RiskCells study. One folder for
   all your feeds is easier to maintain, and RiskCells has only one folder to watch.

RiskCells picks up a new folder within a few seconds.

## PART 6: ADD THE STUDIES TO YOUR CHARTS

How to add a RiskCells study to a chart. Do this for each study, on every chart you want
to send data to RiskCells from:

- A. Click on the chart, then go to Analysis > Studies (or press F6).
- B. Click Add Custom Study.
- C. Find the study's group in the list, click the + beside it, select the study and click Add. The study now appears in the Studies to Graph list.
- D. Select the study in Studies to Graph and click Settings. Its inputs are on the Settings and Inputs tab.
- E. When the inputs are set, click Apply, then OK. Back in the Chart Studies window, click Apply, then OK.

This is how the studies are named in the Add Custom Study list:

| Study | Group in the list | Study name |
|---|---|---|
| Mouse Ticks | Mouse Distance In Ticks | RiskCells™ MouseTicksControl |
| Hourly ATR | ATR Feed 7 | ATR Feed 7 |
| Daily ATR | ATR Feed Daily | ATR Feed Daily |

### MOUSE TICKS

1. Open a chart or DOM of the instrument you trade. Any timeframe works.

2. Add RiskCells™ MouseTicksControl (steps A to E above). Its inputs, in the order you see
   them:

   - Current Price Source (default: Bid)<br>
     The live price the distance is measured from: Bid, Ask or Last Trade.

   - Study Update Delay in Milliseconds (default: 0)<br>
     The shortest time between two calculations. 0 calculates every time Sierra Chart runs
     the study, which is the fastest. A higher number uses less CPU but updates less often.

   - Chart Compression Factor (default: 1)<br>
     Made for compressed charts and DOMs on instruments with big ranges, such as NQ, so
     RiskCells still gets the real tick count your risk is calculated from. The study
     divides the tick distance by this number. Leave it at 1 if the chart's Tick Size is
     the instrument's real tick size. This is also true when you compress with Market
     Depth Combine Increment in Ticks. If you changed the chart's Tick Size, enter the real
     tick size divided by the chart's Tick Size.

   - Round Output (default: On)<br>
     On sends whole ticks. Off sends the exact value with two decimals.

   - JSON Name (default: CUSTOM NAME)<br>
     The name of this feed in RiskCells, for example ES TICKS. Use letters, numbers and
     spaces only, with no space at the end.

   - JSON Write Interval in Milliseconds (default: 100)<br>
     The shortest time between two updates of the feed file. 0 writes every time the study
     runs. Lower is smoother but uses more CPU (see Part 7).

   - Output folder path (default: C:\Users\Public\Documents\\)<br>
     The folder the feed file is written to. Change it to the folder from Part 5, for
     example C:\SierraChart\Data\\, so all your studies write to one folder. The folder must
     already exist.

   - Multi-Chart Mouse Handoff (default: Yes)<br>
     Made so one feed can follow your mouse across several charts. Yes: when charts share
     the same JSON Name, only the chart under your mouse sends its value. No: this chart
     always sends, so only use No when each chart has its own JSON Name.

   - Price Region Only (default: Yes)<br>
     Yes: only the main price area counts. Pointing at a study pane below it (such as
     Cumulative Delta) is ignored, because those panes have their own scale. No: every pane
     counts.

3. In RiskCells, choose this feed in the dropdown of the field you want it to drive. Most
   often that is Stop / Ticks. Then move your mouse pointer over the chart with the study:
   Stop / Ticks follows the distance in ticks from the price to your pointer, and Contracts
   is recalculated from it straight away. Sierra Chart shows the same distance as
   "Ticks Away" at the top of the chart.

   Note: when a calculator's ATR field has a value, RiskCells works out Stop / Ticks from
   the ATR instead, and the Mouse Ticks value is replaced. On the calculator you use for
   Mouse Ticks, turn ATR off with its ATR button.

Good to know:
- The feed file is created the first time you move your mouse over the chart, in the
  folder set in Output folder path.
- Using several charts? Add the study to each chart with the same JSON Name. Only the chart
  under your mouse sends its value, so RiskCells follows the chart you point at.

### HOURLY ATR

1. Open a 1-hour chart (60-minute bars) of the instrument.

2. Add Sierra Chart's Average True Range study: go to Analysis > Studies, select Average
   True Range in the Studies Available list, click Add, then Apply and OK. To use a
   different ATR period, open its Settings and change Moving Average Length.<br>
   Note: you don't have to use ATR. The studies are called ATR Feed, and ATR is the name of
   the button in RiskCells that shows these fields, but RiskCells does not care what the
   value is based on. You can point the study at any other Sierra Chart study as your
   volatility input.

3. Add ATR Feed 7 (steps A to E above). On the Settings and Inputs tab, set:
   - Instrument name: the name RiskCells shows for this feed, for example ES 1H.
   - ATR source (chart, study, subgraph): this chart, then Average True Range (or any other
     study you want to use), then its subgraph.
   - Output folder path: the folder from Part 5. We recommend your Sierra Chart Data
     folder, C:\SierraChart\Data\\, which is already the default. Keep all your RiskCells
     studies writing to this one folder: it is easier to maintain, and RiskCells has fewer
     folders to watch.

   Click Apply, then OK. Back in the Chart Studies window, click Apply, then OK.

4. In RiskCells, choose the feed (for example ES 1H) in the dropdown above the ATR field. DYN turns on by itself and the ATR field fills (see ATR MODES below).

Tip: leave the contract month out of the name and add the timeframe instead, so the feed
is easy to find later, for example ES 1H.

### DAILY ATR

1. Open a daily chart (1 day per bar) of the instrument.

2. Add the Average True Range study (or the study you want to use), the same way as for the
   hourly chart.

3. Add ATR Feed Daily (steps A to E above). On the Settings and Inputs tab, set:
   - Instrument base name: for example ES. The study adds -D1 for the daily timeframe, so
     the feed shows as ES-D1.
   - ATR source: this chart, then Average True Range (or your chosen study), then its
     subgraph.
   - Output folder path: the same folder as the hourly study.

   Click Apply, then OK. Back in the Chart Studies window, click Apply, then OK.

4. In RiskCells, choose ES-D1 in the dropdown above the ATR field. DYN turns on by itself and the ATR field fills (see ATR MODES below).

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

### SAVE YOUR CHARTBOOK

When your studies are in place, choose File > Save in Sierra Chart so they are there the
next time you open it.

## PART 7: SMOOTHER UPDATES (OPTIONAL)

Sierra Chart limits how often studies like these run, and RiskCells reads Stop / Ticks and
ATR feeds every 100 ms by default. For a smoother Stop / Ticks value you can make both
faster. Faster updates use more CPU, so read the warning below first.

In Sierra Chart, on each chart that has the Mouse Ticks study:

1. Go to Chart > Chart Settings > Performance. Set "Minimum Chart Update Interval In
   Milliseconds For ACSIL UpdateAlways" to 50 (it is usually 300).

2. In the same window, on the Display tab, set "Chart Update Interval in Milliseconds" to
   50. (0 means the chart uses your global setting.) Click Apply All, then OK.

3. Open the Mouse Ticks study's settings (Analysis > Studies, select the study, Settings).
   Set "JSON Write Interval in Milliseconds" to 0, so the study writes every time it runs.
   Click Apply, then OK. Back in the Chart Studies window, click Apply, then OK.

If you don't see the Performance setting, update Sierra Chart. ATR changes slowly, so your
ATR charts can stay as they are.

In RiskCells, in your main window:

4. Open Master Settings > Risk Parameters. At the bottom you can set how often RiskCells
   reads each type of feed, in milliseconds (10 to 5000):
   - ATR Poll ms (default 100): ATR feeds
   - Stop Ticks ms (default 100): Stop / Ticks and Contracts feeds
   - Live R ms (default 1000): feeds chosen for R, and the live feeds in Risk Parameters
   - Monitor Widget ms (default 1000): the values in your Monitor Cells

   For smoother Mouse Ticks, set Stop Ticks ms to 50.

5. Click Restart now when RiskCells asks. The new rates apply to all windows after the
   restart.

### WARNING

- Faster updates cost CPU in both Sierra Chart and RiskCells.
- Sierra Chart does not recommend chart update intervals below 100 ms, and asks users not
  to contact its support about problems caused by very short intervals.
- Use short intervals only on the charts that need them, never in Sierra Chart's global
  settings.
- Very fast poll rates also make RiskCells work harder, especially with many feeds and
  windows open.
- If Sierra Chart or your PC starts to lag, raise the numbers again, for example to 100.

## PART 8: CHECK THAT EVERYTHING WORKS

- "Ticks Away" at the top of your Sierra Chart chart changes as you move the mouse.
- In RiskCells, the indicators beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in the calculator's ATR field.

### HOW TO READ THE INDICATORS

Each feed dropdown has its own indicator, and each row has a master indicator next to the
row name.

Feed indicator:
- Blue: the feed is updating.
- Pink: no update for about 8 seconds, or the feed has no usable value. The last value
  stays in the field.
- Grey: MANUAL, no feed selected.

Master indicator, for all the feeds selected in that row:
- Blue: every selected feed is updating. It is also blue when no feed is selected.
- Yellow: at least one feed has stopped while others are updating. Look for the pink
  indicator in that row.
- Pink: none of the selected feeds are updating.

These are the default colours. You can change them in Master Settings > Graphic Settings.

## TROUBLESHOOTING

**The studies are not in the Add Custom Study list**
- Check that the three DLL files are in the Data Files Folder shown in Global Settings >
  General Settings > Paths.
- Right-click each DLL file, choose Properties, tick Unblock if you see it and click OK.
  Then restart Sierra Chart.
- Antivirus software can block downloaded DLL files. Check that it has not blocked them.
- Make sure Safe Mode is not ticked on the Sierra Chart login window.
- Make sure you extracted the three DLL files from the zip file. Sierra Chart can't use
  them while they are still inside the zip.

**A feed is missing from the RiskCells dropdown**
- Mouse Ticks: move your mouse over the chart's price area. The file is created on the
  first movement, and Sierra Chart must be connected to market data.
- Check that the folder in the study's Output folder path is listed in Feed Folders and
  switched on.
- Look for the name you gave the study: its JSON Name, its Instrument name, or its base
  name with -D1 added (Daily ATR).

**Stop / Ticks does not follow my mouse**
- Select the Pointer tool in Sierra Chart (Tools > Pointer).
- Point at the price area, not at a study pane below it.
- If the calculator's ATR field has a value, Stop / Ticks is worked out from the ATR
  instead. Turn ATR off on that calculator with its ATR button.
- Using the same JSON Name on several charts and you closed the chart that was sending?
  Move your mouse over another chart with that name. It takes over within a few seconds.

**A feed indicator is pink**
- RiskCells has had no update from that study for about 8 seconds. Check that Sierra Chart
  is open and the study is still on the chart.
- For an ATR feed, check that DYN or LOCK is on.

**ATR shows 0**
- Check that DYN or LOCK is on.
- Open the ATR study's settings and set ATR source to the Average True Range study (or the
  study you chose) on that chart.

Need help? Email info@riskcells.com.
