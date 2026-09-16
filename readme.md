# RiskCells

## Contents

- [About RiskCells](#about-riskcells)
  - [The software](#the-software)
  - [Platforms](#platforms)
  - [Licence & devices](#licence--devices)
  - [Features](#features)
- [Onboarding](#onboarding)
  - [NinjaTrader](#ninjatrader)
  - [Quantower](#quantower)
  - [Sierra Chart](#sierra-chart)
  - [TradingView](#tradingview)

## About RiskCells

### The software

#### What does RiskCells actually do?

RiskCells is a desktop application that sits next to or on top of your trading platform and calculates risk per trade, stop distance, position size and other variables for different instruments, using fully customizable inputs that can be entered manually or supplied live. Its account-monitoring and execution cells can respond to the same live workflow.

It also includes a native hotkey execution engine, account monitoring and independent WindowPanels. Every cell and every window is individually customizable, can be resized and styled, and can live on its own or alongside other cells in any configuration across one or multiple monitors. RiskCells is designed as a separate control layer around your workflow, to enhance your trading platform and your efficiency, not to replace them.

#### Who is RiskCells for?

RiskCells is for active intraday traders who want to improve the speed and efficiency of their risk calculation and execution.

It produces the most value for traders who trade multiple markets and run multiple strategies, each requiring different risk parameters that are not easy to calculate on the spot in a fast-moving market on a busy day. Futures traders on the CME or Eurex exchanges know this best: one contract is 12.50 dollars per tick, another is 6.25, and so on. RiskCells aims to eliminate the delay caused by the calculations an active trader has to perform by hand many times a day, by streamlining R values with multiple risk parameters and input settings that can be used in real time. These range from a day trading daily stop (DTDS) to the Kelly criterion or a fixed account percentage as risk, and they can be adjusted for you in real time by the account feed inputs or set manually.

RiskCells is also the perfect solution for traders who use several platforms at once. It acts as a single control surface for all your platforms and system applications by sending keystrokes to whichever window you assign to the ControlCell, which lets you toggle between its hotkey window targets with one click. With multiple window targets per ControlCell, multiple ControlCells per window and multiple windows per monitor, the possibilities are endless.

#### Which cells are included?

Every plan includes the RiskCell, a position-sizing and volatility-monitoring tool; the ControlCell, a native C++ keystroke and macro engine; and the MonitorCell, which watches supported account data in real time. Profiles let you save settings for different instruments, accounts, strategies and workflows, and those settings persist between app restarts. ControlCell configurations can be saved as profiles as well.

Each cell can be opened independently, combined with other cells, resized, restyled and arranged differently in each WindowPanel. The ControlCell can send keystrokes to any Windows application that accepts them, not only trading platforms, so it can also control browsers, screenshots, OBS or other recording tools, system functions and similar workflows. Repeat rates, timed sequences and multi-action macros let one trigger perform several actions with configurable delays.

If you have a cell idea, improvement or bug to report, use the contact form. Those requests help us focus development where users need it most.

#### Does it place trades for me?

No. RiskCells never trades on its own. It is separate from your broker and trading platform and does not use their trading APIs or hold broker credentials. The ControlCell is a configurable keystroke layer: it sends the keystrokes you define to the Windows application or window you choose, exactly as if you had pressed them yourself, and only when you trigger it.

That same layer can control more than trading software. You can use it for browser shortcuts, screenshots, OBS or recording controls, system functions and other applications that accept keyboard input, including repeat rates and timed multi-action sequences. What any target application does with those keystrokes is governed by that application, which is why we recommend testing every trade-related hotkey and macro in simulation first.

#### What are the system requirements?

RiskCells runs on 64-bit Windows 10 and Windows 11, but we strongly recommend Windows 11. Most features work the same on Windows 10; however, we have observed differences in some operating-system components, particularly around voice control, and we cannot guarantee that every feature or the overall performance will match Windows 11. Microsoft has ended standard support for Windows 10, so it also no longer receives the same ongoing security and feature updates as Windows 11. We will maintain general compatibility where practical, but new development and optimization will be focused on Windows 11.

If you use macOS, Linux or another operating system and would like RiskCells support there, please contact us. We track those requests as a development data point.

### Platforms

#### Which trading platforms are supported?

Custom studies and indicators currently ship for NinjaTrader, Sierra Chart and Quantower, with Rithmic R Trader Pro supported for account metrics. A platform is supported when we have already built and tested the study or indicator for it, so the integration works out of the box. The keystroke engine is separate and drives any Windows application that accepts keyboard input, and manual mode gives you the full position-sizing workflow anywhere.

Being technically capable of writing the data RiskCells reads does not by itself make a platform supported. Most web-based platforms cannot write it at all; the desktop platforms that can are exactly the ones we are working to integrate next. Tell us which platform you want through the survey, our social channels or by email, and it feeds directly into what we build.

#### What makes a platform supported?

RiskCells reads local JSON files carrying the live values it needs: stop distance and volatility for position sizing, account metrics such as balances, and the data behind the macro functions of the native keystroke system. Supported means we have written and tested the study or indicator that produces those files for that platform.

Platforms we have not yet built that layer for are candidates rather than supported, and that list keeps growing. We work with the community on which platforms and which features come next.

#### Does it work with Rithmic accounts?

Yes. Rithmic is supported, and the MonitorCell shows the balance, drawdown and daily figures your account data provides.

There is more than one way in. Rithmic R Trader Pro writes a continuous CSV that you can point RiskCells at; it converts and displays the account data your provider supplies, including balances and margins. If you run your Rithmic connection through NinjaTrader or Quantower, you do not need that CSV at all, because the platform studies already carry the account data, unless you specifically want the R Trader Pro fields or a combination of both sources. Write speeds vary between sources and platforms.

#### Can I use it across multiple monitors?

That is what the WindowPanels are for. Open up to twenty windows per instance and place them on any screen. A single window can hold several RiskCells modules, several ControlCells and several rows of MonitorCell fields, and each window is customised on its own: its profiles, strategies, feed inputs, keystrokes, styling and always-on-top behaviour. Windows can be saved and renamed individually, and they reopen exactly where you left them, so RiskCells comes back positioned around your platform the way you built it.

A Stream Deck plugin is included so hotkeys and risk presets can live on physical buttons. It binds by proximity: the Stream Deck listens to and executes on the RiskCells window nearest your cursor, and when your windows are spread over several monitors it follows the mouse to the monitor you are working on, then to the closest window on it.

### Licence & devices

#### How many devices can I use?

The number of devices you subscribe to on your licence at checkout. An Individual licence covers one or two machines, which suits a trader working from a single desk or across two. A Lifetime licence covers two machines. An Enterprise licence covers ten or twenty, for trading teams, trading floors, trading rooms and communities.

The only difference between the plans is how many devices can be logged in on the same login. Every feature is included on all of them.

One email address can hold only one subscription, so two Individual or Enterprise subscriptions cannot be combined. To get more devices on a subscription, change your plan in the customer portal. A lifetime licence is a separate one-time purchase and can be held alongside a subscription on the same email address; their devices then add up, so a Lifetime licence for two machines plus an Enterprise subscription for ten gives you twelve.

#### Can I move my licence to a new computer?

Yes. Open About inside RiskCells, go to ACCOUNT and then DEVICES. Every machine currently using a seat is listed there with its name and when it was last seen, and each row has a RELEASE button. Release the old machine and sign in on the new one. Moves are free.

That list is the answer even when the old machine is gone, broken or already wiped: you release it from the new machine, so you never need access to the old one. Logging out of a machine you still have also frees its seat.

If you sign in on a new machine while every seat on your plan is in use, RiskCells shows you the machines that hold them and lets you release any of them, so you are never locked out of a licence you have paid for.

#### Who can remove a machine from the licence?

Only the owner of the email address the licence was bought with, who can read its inbox. Freeing the seat of the machine you are sitting at needs nothing but that machine. Freeing any other machine sends a one-time code to the account address and asks you to enter it, so removing someone else's machine requires control of the inbox.

To be clear about what this is not: there are no per-person logins and no administrator account. A licence has devices, not members. Only the email owner who can read the account inbox can add a machine or remove one, because both actions require the one-time code.

Removing a machine frees its device slot, so another machine can take it.

#### What happens if I move to a plan with fewer devices?

A downgrade takes effect at the end of the period you have already paid for. From then on, the machines used most recently keep their seats. If more machines are signed in than the new plan covers, the ones used least recently are signed out.

The same happens if you hold a lifetime licence and a subscription on the same email address and one of them ends.

The owner of the account's email address can sign in on any computer, with that address and a one-time code. If every seat is in use, the sign-in screen lists the machines holding them and can release any of them to sign in there. They can also be released from the app under About › ACCOUNT › DEVICES on a signed-in computer.

Only the owner of that email address can add or release machines: each sign-in and each release of another machine needs a one-time code sent to that address, so a machine that is still signed in cannot remove anyone else. A machine can always sign itself out.

#### How does Enterprise work?

One licence for a whole group. It is built for trading desks, trading teams, trading rooms and communities such as Discord groups, where several people run RiskCells on their own machines under a single purchase. Ten or twenty machines can hold a seat at the same time, and every seat gets the complete product.

The group shares one account and one email address. Every machine signs in with that same address, so there are no separate accounts to buy and nothing to set up per person.

The owner of that email address controls the licence through its inbox. A code is sent there the first time a machine signs in, and again whenever someone frees another machine's seat, so the person who bought the licence decides who joins and who leaves. After that first sign-in a machine remembers, and every later start is silent.

We advise licence holders to keep an internal record of the device names of the people they share the licence with, or to ask them to name their machines for easier entitlement management. Windows names devices in a non-obvious way, such as "DESKTOP-4F9K2A", which can cause confusion and mistakes.

#### Do I need to be online to use it?

Yes, but not continuously. RiskCells needs an internet connection to verify your licence from time to time. Between those checks your position sizing, hotkeys and platform feeds all run locally, so a brief drop mid-session will not interrupt your trading.

### Features

#### Settings

##### Master Settings
The "Master Settings" panel is the control centre of RiskCells. Every setting in the application lives here, organised into five groups: Interface, Graphic Settings, Voice Control, Interface Sounds and Risk Parameters. Each group opens and closes on its own, so you only ever see the controls you are actually working with. It keeps a deep and highly configurable system genuinely easy to navigate.

RiskCells separates settings into global and local. A global setting is owned by the master window and applies everywhere the moment you change it, keeping your whole workspace consistent without having to repeat yourself. A local setting belongs only to the window you are in, which is what allows every window to look and behave differently. That split is deliberate, and it is what makes RiskCells as simple or as intricate as you want it to be. Keep your RiskCells clean and simple if that is all your strategy requires, or build in all the complexity you need to reach the precision you are after. The goal throughout is serious depth of control that never becomes complicated to reach.

*Note: Master Settings holds the settings that govern the application and its windows. Each cell also carries its own settings, kept with the cell itself so that the controls you need are always close to the thing they affect.*

##### Window Picker
The "Window Picker" is where you open, close, name and manage every RiskCells window. RiskCells runs up to 20 windows, and each one is a completely independent workspace with its own cells, calculators, feeds, colours, fonts and layout. Tick a window to open it, untick it to close. Nothing is lost when a window closes: its size, position, screen, always-on-top state and execution mode are all remembered, so it returns exactly as you left it. Any windows still open when you quit will reopen automatically the next time you launch RiskCells.

Double-click a window's name to rename it, which lets you label windows by instrument, strategy, monitor or desk. "+ Add Window" reveals the next available window, and the "−" button hides a window's row from the list. Hiding is not deleting. A hidden window keeps its entire configuration, so you can bring it back at any point and it will open exactly as it was.

*Note: The first window is the master window and stays open for as long as RiskCells is running, so closing it closes the application. Every other window is fully independent, both of the master and of each other.*

##### Save / Load Profile
The "Save / Load Profile" feature lets you capture a snapshot of your entire configuration, covering risk parameters, feed settings, cosmetic styling, colors, and profiles. You can create multiple profiles for different instruments, strategies, or feed setups. At any time, summon a saved profile into any window, allowing you to adjust instantly to your trading needs, market conditions, or desired style.

*Note: The profile includes Control Cell setups. However, Control Cells also have their own save/load mechanism for even more granular strategy or execution configurations. This allows traders to switch rapidly between different execution styles, conditions, or macro needs.*

##### Always on Top
The "Always on Top" function allows each RiskCells window to remain above other windows independently. You have full control to toggle this on or off for each specific window. This ensures that you can prioritize exactly which RiskCells views stay visible, depending on your active execution or monitoring needs. Each window’s visibility is managed separately, giving you tailored focus across trading monitors and window configurations.

##### Execution Mode
The "Execution Mode" turns a RiskCells window into a dedicated hotkey execution tool. Windows itself treats the window as a tool rather than a normal application, so it never takes focus away from your trading platform no matter how much you interact with it. Your platform stays focused the entire time, and that is what makes instant hotkey delivery possible. Execution Mode is set per window, so you can put the windows you trade from into Execution Mode and leave the ones you type and configure in exactly as they are.

The native Windows C++ keystroke sender works in every mode. What Execution Mode removes is the operating system's focus-shift delay. A keystroke can only reach your trading platform if that platform is focused at the moment the keystroke is sent, so in normal mode RiskCells has to hand focus over at the instant you click, and Windows charges time for that handover. Execution Mode uses time you are already spending: hovering a Control Cell button pre-focuses the target window, so by the time you click, focus is already there and the keystroke goes out immediately. Your pointer has to travel across the button regardless, so the handover costs you nothing. This is the recommended way to use Control Cells whenever keystroke execution speed matters.

An added benefit of the prefocus hover is that it also brings the target window to the front, above every other application, except for RiskCells. If you run several DOMs or platform windows at once, whichever one a Control Cell is pointed at is raised and focused the moment you reach for its button.

Execution Mode also enables Always on Top automatically. A window that can no longer be clicked into focus has to stay visible above everything else, so the two behaviours work as one.

*Note: Keyboard input into a window in Execution Mode is disabled by design, which is the trade-off for never stealing focus. Steppers will appear on every numeric field whenever a window is in Execution Mode, each with its own individually configurable increment settings, so every value stays precisely adjustable with the mouse alone.*

#### RiskCell

##### Settings
The Risk Cell's own "Settings" hold everything that shapes this cell: how many modules and calculators it carries, how wide they sit, the colours of every field and button, the decimal behaviour of each value, and the edges, borders and typography that make the cell yours. These are local settings, so they change this cell in this window and leave every other window alone.

Keeping the settings on the cell itself means the controls are always next to the thing they affect. You are never hunting through a global menu to change one number on one calculator.

##### Name Field & Tick Value
The "Name Field" labels a row so you always know what you are looking at. Beside it sits a colour indicator, and together they are how you tell your instruments apart at a glance. Give a row its name and its own colour, and the frame of that entire row takes the colour with it. Blue for your index work, amber for energy, a colour per strategy or per session, whatever lets you read your layout instantly without stopping to check. When several instruments are on screen at once, colour is what stops you reading the wrong row at the wrong moment.

The "Tick Value" is the dollar value of a single tick for that instrument, and it is what turns a stop distance into money. It is shared by every calculator in the row, which is the reason rows exist: one instrument, one tick value, several calculators working from it. Set it once and every calculator in that row sizes correctly.

*Note: Tick Value is the denominator of the position sizing calculation. Until it is set, the calculators in that row have nothing to size from and will show zero contracts.*

##### C1-C4 Macro Feed
The C1-C4 buttons hand a calculator's position size straight to your Control Cell. Press C1 and calculator 1 becomes the size behind every linked Control Cell button in that window, so a button set to repeat fires exactly as many times as your calculated contracts, and keeps up as your risk, your stop or volatility move that number. Press the lit button again and it switches off, dropping those buttons back to a single shot. Press a different one and the source changes instantly.

This is the join between sizing and execution. The Risk Cell works out the repeat rate based on its live feed input, and the Control Cell sends it, without you carrying the number across in your head or typing it into a macro by hand. One press decides which calculator is driving, and from then on the size on screen is the size that fires.

Use this feature with the utmost care and attention. It is for professionals only: one keypress becomes as many keystrokes as your calculator says. Where those keystrokes can be tied to orders, every broker, data provider and prop firm sets its own rules on how orders may be sent and received, and many throttle platform input for basic accounts. Do your own research and calibrate RiskCells to your provider's criteria.

Right-click does something else entirely: it compacts that one calculator. RiskCells also has a master compact, the "C" in the RiskCell's control bar, that shrinks every calculator in the window at once, and a calculator with its own pin set stays compact when the master is switched back off.

*Note: C1-C4 appear only on the first module's calculators, up to four of them, because those are the only values a macro can be driven from. Every other calculator carries a plain "C" in the same place on the calculator itself, which compacts on either click. The compact pin applies to the vertical calculator layout and is saved with your profile.*

##### Feed Selector
The "Feed Selector" is what connects a calculator to live data. Point any of the value fields at a feed, choose which number inside it you want, and that field updates itself from then on.

RiskCells reads plain JSON files, and that is the whole requirement. Any JSON file placed in a folder you have pointed RiskCells at, containing at least one numeric value, becomes a feed you can select. There is no schema to conform to, no registration, no approval. Add a folder and RiskCells picks it up within seconds. If a file carries more than one number, RiskCells finds them all and lets you choose which one drives the field.

We supply ready-made studies and indicators for the major platforms that support them, so most traders are connected within minutes. See Resources. But the format being open is the point: if you can produce a number, you can feed it to RiskCells. Write your own study, export from a spreadsheet, or vibecode a script that outputs whatever variable your strategy actually depends on, and RiskCells will read it and size from it. Your risk model does not have to be one somebody else imagined for you.

*Note: RiskCells reads files from folders on your own machine. It does not connect to a broker or an exchange, and it places no orders.*

##### Live / Stale Indicator
The "Live / Stale Indicator" tells you whether the data behind a value is actually arriving. Green means the feed is updating. Red means it has stopped. Each row also carries a master indicator that summarises every feed in that row at once, including a partial state for when some feeds are running and others are not, so a single glance tells you whether everything is healthy.

This matters because a stale feed is not an obvious failure. The number stays on screen and looks perfectly reasonable, and RiskCells deliberately keeps showing you the last value it received rather than blanking the field. The indicator is what tells you that the number in front of you has stopped moving.

Every part of it is yours to style. The live, stale and partial colours are each fully customisable, as is the glow around them, which can be softened or switched off entirely. If the indicators do not suit how you work, they can be turned off altogether, independently for the feed indicators and the row master indicator. Match them to your platform, match them to your theme, or remove them from view completely.

##### Global R
"Global R" and "Local R" keep your risk figure in step across calculators, so a single change reaches everywhere it should without you retyping it. Local R links every calculator inside the window you are in. Global R extends that across every window running RiskCells. Between them sits a set of group links, which tie together matching calculators across your modules so you can sync a chosen subset rather than everything at once.

That range exists because traders work differently. Some carry the same risk across every instrument they touch and want one number to move everything instantly. Others want a specific group in step, holding their index and their energy setups on separate risk while day and night sessions run apart, or while conditions change through the session. RiskCells lets you be as broad or as granular as your strategy calls for, and lets you change your mind mid-session by pressing one button.

What syncs is the dollar risk, never the position size. Each calculator keeps its own stop and its own tick value, so linked calculators land on the same risk and then size themselves independently for their own instrument. That is the entire point: one decision about what you are willing to lose, correctly translated into a different number of contracts for every market you are in.

*Note: Global R is opt-in at both ends. A window only accepts an incoming risk change if it has Global R switched on itself, so a window you have deliberately left independent stays independent.*

##### Voice Input
"Voice Input" lets you set your risk and your stop by speaking, without leaving your chart or touching the keyboard. Say "risk 350" or "stop 18" and the value changes in real time, and your position size recalculates with it. Volatility modes can be switched by voice too, so you can move a calculator between its dynamic, peak and locked states while your hands stay where they are.

Each calculator decides its own relationship with your voice. A calculator can listen continuously, respond only while you hold a push-to-talk key, or ignore voice entirely, so you choose exactly which values your voice is allowed to move.

Spoken feedback is optional. Leave it on and RiskCells reads your new contract size back to you, which means you never have to look away to confirm a change landed. Turn it off and the numbers simply change on screen. You can pick the voice that reads them.

*Note: Voice recognition is tunable to your room and your microphone. The noise gate, how long a pause ends a phrase, the minimum length of a phrase and the push-to-talk release timing are all adjustable, alongside microphone selection and how spoken input is routed between your open windows.*

##### ATR Mode
"ATR Mode" is what makes a stop respond to market conditions instead of sitting at a fixed number. With it on, your stop is derived from a volatility reading and the percentages of it that you choose, so as the market expands and contracts your stop follows, your contract size adjusts underneath it, and your dollar risk stays exactly where you put it.

When RiskCells detects a feed carrying volatility data, extra controls appear on the calculator. DYN tracks the current reading and keeps moving with it. MAX works from the session's peak instead of its current value, for when you want to size against the worst the session has offered rather than the moment you happen to be in. LOCK freezes the calculation onto one specific reading, chosen from a selector that fills itself from the feed's own history: a particular hour of the day, or a particular day of the week. The options you see are whatever your feed actually contains, so a locked stop is always anchored to a real historical reading rather than a guess.

It does not have to be ATR. RiskCells detects the structure, not the subject. Any output built the same way is treated identically and gets the same controls, so you can drive your stops from any measure your strategy trusts. See Resources for the structure. We ship ATR studies for the supported platforms because it is a reliable and universal measure of volatility and it suits most traders out of the box, but in an environment like Sierra Chart you can point the study at any output you like, and RiskCells will read it and size from it exactly the same way.

*Note: A volatility feed carrying a tick size is converted to ticks for you automatically, so the number you size from is already in the units your stop is measured in.*

##### Pause Feed
"Pause Feed" hands a value back to you for a moment without dismantling anything. Trading rarely runs in a straight line, and there are constant moments where you want to try something: check what a different stop would do to your size, work out what a setup would have cost at another risk level, or answer a quick "what if" that has nothing to do with what the feed is telling you. Pause, do it, unpause, and the feed picks straight back up.

Paused fields stay fully editable, so you can type into them, step them, or speak to them exactly as if they were manual. Nothing about your configuration changes. Your feed stays selected, your settings stay put, and unpausing resumes the live value immediately with no reconnection and no setup to redo.

*Note: Pausing a risk feed hands back the value you had before the feed took over, so you return to your own number rather than a frozen copy of the feed's. The other fields hold their current value in place until you release them.*

##### Lock Contracts
"Lock Contracts" inverts the math. Normally you set your risk and RiskCells calculates the position size. With Lock Contracts on, the Contracts field becomes the input and Risk becomes the output, so you set a size and RiskCells tells you what it costs you:

Risk = Contracts × Stop Ticks × Tick Value

This answers the opposite question, and it is the one traders ask constantly. What is this size actually worth to me at this stop distance? Size up or down and watch the dollar figure move with it. Widen or tighten the stop and see the same. Because the stop can still be driven by ATR while contracts are locked, you can hold a fixed size and watch your real exposure change as volatility moves, which is difficult to see any other way.

It is equally useful in reverse, for reading a position you are already in. Put in the size you are holding and the stop you are working with, and the dollar figure in front of you is what is genuinely on the line.

*Note: Your original risk figure is stored the moment you lock and handed straight back when you unlock, so a Lock Contracts session never costs you the setup you had before it. While locked, that calculator holds its own risk value and stops taking risk updates from feeds or from linked calculators.*

##### Risk ($ per Trade)
The "Risk" field is the dollar amount you are prepared to lose on a single trade, and it is the value the rest of the Risk Cell is built around. Type it in, adjust it with the steppers, speak it, sync it across calculators, or let RiskCells work it out for you automatically.

RiskCells gives you two automatic sizing models, both configured in Risk Parameters. DTDS works downward from a daily limit: you set your account size, then a daily loss limit as either a dollar amount or a percentage of the account, then divide that across the number of trades you expect to take, which gives your risk per trade. ACC % works in a single step, taking your risk per trade directly as a percentage of your account. Each model comes in a static and a live version. Static uses the figures you type. Live reads your account balance straight from a connected feed and recalculates continuously, so your risk compounds up and down with your account without you ever adjusting it. An optional modifier lets you offset the balance the calculation works from, positively or negatively.

*Note: "Risk Decimal" in the settings hides the decimals on a calculated or fed Risk value. When the value arrives from a feed, the shortened figure is the one that drives the math, so what you see is exactly what is being used.*

##### Contracts (Auto)
The "Contracts" field is your position size, and RiskCells calculates it for you:

Contracts = Risk ÷ (Stop Ticks × Tick Value)

It recalculates the instant anything it depends on changes, whether that is you typing a new risk figure, an ATR feed moving your stop, or a live account balance shifting your risk per trade. The result is displayed to two decimal places rather than rounded to a whole lot, so you can see exactly where a size falls and make your own decision about how to round it.

*Note: Contracts can also be driven the other way around. See "Lock Contracts".*

##### Stop / Ticks
The "Stop / Ticks" field is your stop distance measured in ticks, and it is the second half of the position sizing equation. It can be typed in manually, taken from a feed, or calculated for you from volatility.

When ATR Mode is on, your stop is derived automatically as a percentage of the current ATR reading, and the percentages themselves are yours to set. Your stop then moves with market conditions, widening as volatility rises and tightening as it falls, and your contract size adjusts with it in real time while your dollar risk stays exactly where you set it.

*Note: A separate decimal setting rounds the calculated stop to whole ticks. The rounded figure is the one used in the sizing math, so the displayed stop and the stop being calculated from are always the same number.*

#### ControlCell

##### Drag Handle
The "Drag Handle" moves the Control Cell wherever you want it. Cells snap to each other and to the window edges as you drag, so building a clean layout takes seconds.

##### Cell Settings
The Control Cell's "Settings" control how the cell is built and how it looks: how many buttons across, their width, height, text size, borders, edges, gradients and zoom, along with the full setup of the three button indicators (see "Hotkey"). These are local settings, so every Control Cell can be sized and styled completely independently of the others.

##### Save / Load Cell
"Save / Load Cell" stores a Control Cell as a named profile you can recall at any time. Profiles are keyed by name, so saving over a name replaces it and saving under a new one adds it, and there is no limit on how many you keep.

The reason to keep several is that a Control Cell is a working layout, not a fixed tool. A scalping layout and a swing layout want different buttons in different places. A cell built around one platform will not match another's. Different sessions, instruments and strategies each justify their own arrangement, and moving between them should take a moment rather than a rebuild. Profiles are stored centrally, so a cell you save in one window can be loaded into any other.

*Note: A profile carries the cell's buttons, layout, colours, sizing and indicator setup. It deliberately does not carry your target windows or the hotkeys bound to them. Those stay with the live cell, so loading a profile can never route keystrokes somewhere you did not intend on that machine. On load, RiskCells rebinds the buttons to this window's own targets and tells you how many came through with live hotkeys.*

##### Target Window
The "Target Window" buttons decide where a Control Cell's keystrokes go. A cell holds up to four, each pointing at a window on your computer. Blue means the target is live and will receive keystrokes. Grey means it is set up and switched off. Click one to toggle it, double-click to rename it, and right-click to choose which window it points at.

This is what makes switching platforms effortless. Set up a target for each platform or order window you use, then move between them by clicking. You are not rebuilding buttons or remapping hotkeys, only changing which target is lit. Activate more than one and a single press fires to all of them in turn, each to its own window with its own timing, which is how one button drives several DOMs or several platforms at once.

RiskCells controls your machine, not the market. A Control Cell sends hotkeys and keystrokes to the window you select, exactly as if you had pressed those keys yourself with that window focused. It places no orders and communicates with no broker or exchange.

*Note: In Execution Mode, hovering a button pre-focuses and raises its target window before you click, so the keystroke lands the moment you press (see "Execution Mode"). If a target window has closed, RiskCells marks it and blocks the keystroke rather than sending it to whatever happens to be focused.*

##### Refresh Windows
"Refresh Windows" re-scans every window open on your computer and re-checks each of your targets against it. Use it after opening a platform, restarting one, or whenever your window layout has changed.

Any application window on your machine can be a target, not only trading platforms. RiskCells reads the list of open windows and offers you everything it finds, which is what opens the door to the wider automation (see "Control Button").

##### Close Cell
Closes the Control Cell. Its buttons, hotkeys and targets are kept, so reopening brings it back exactly as it was.

##### Control Button
A "Control Button" sends keystrokes. That is the whole of what it does, and it is precisely why it is so flexible: whatever a keystroke can do on your computer, a Control Button can trigger.

Each button holds up to five keystrokes, fired in sequence, and every one carries its own delay. A single press becomes a scheduled routine: one keystroke now, another a fraction of a second later, a third after that. Double taps, triple taps, multi-key sequences, timed follow-ups. Anything you can press by hand you can map, modifiers included. When you fire to several windows at once, each target sends its own keystroke on its own timing.

The reach goes well past your trading platform. Because a target can be any window on your machine (see "Target Window"), one press can drive several applications together. Send your trading command to your platform, then 100 milliseconds later send a screenshot command to your capture tool, so every entry documents itself without you thinking about it. Trigger a recording marker in OBS. Fire anything at all that responds to a hotkey. The trade and the record of the trade become a single action.

*Note: Each button also carries a repeat count (see "Repeat Rate") and can be linked to others (see "Linked"). Its three indicators show its hotkey, its repeat rate and its link state at a glance (see "Hotkey").*

##### Hotkey
The "Hotkey" indicator is the small chip on a button showing which keystroke it will send, so you never have to remember or guess what a button does.

All three indicators (hotkey, repeat rate and link state) can be dragged to any corner of their button and stack neatly when they share one. They can be resized, recoloured from a single swatch or set to follow each button's own text colour, given their own transparency, and squared or rounded to match your theme. Each can be switched off on its own if you want the cleanest possible button face.

We recommend leaving them on. A Control Cell button is something you press quickly, often, and frequently under pressure, and the indicators are what tell you at a glance that you are about to press the right one.

##### Repeat Rate
The "Repeat Rate" indicator shows how many times a button fires its keystroke on a single press. A button set to repeat sends its keystroke that many times in a row, with a delay of your choosing between each.

Its real power is that the count can be driven by your position size automatically. Link a button to one of your calculators and its repeat rate becomes that calculator's contract count, updating continuously as your risk, your stop or market volatility change. Your calculated size becomes the number of times your order hotkey fires, so sizing and execution can never drift apart. You choose which calculator drives it, and you can apply a multiplier, control how fractional sizes round, and set a hard ceiling the count can never exceed.

*Note: A repeat rate can be paused, sending a single keystroke while leaving the whole setup intact. The indicator shows when a button is paused, so a paused macro is never a silent surprise.*

##### Linked
"Linked" ties a group of buttons together so their macro settings move as one. Change the repeat rate on any linked button and every other linked button follows instantly. Point one at a different calculator and they all follow.

This is what keeps a multi-button cell manageable. A Control Cell often holds several buttons that all need to fire at your current position size, and without linking every size change means editing each of them in turn. Linked, they behave as a set, and your whole cell stays in step from a single adjustment.

Linking covers the macro behaviour only: the repeat rate, the delay between repeats, and which calculator drives them. Hotkeys, colours and targets stay individual, so linked buttons still do their own separate jobs.

*Note: A linked group can be paused and resumed together, so you can drop an entire set to single-shot and bring it back without touching them one at a time.*

#### MonitorCell

##### Drag Handle
The "Drag Handle" picks the Monitor Cell up and puts it anywhere you want it. Cells snap to each other and to the edges of the window as you move them, so a tidy layout takes seconds rather than pixel-nudging.

##### Monitor Settings
The Monitor Cell's "Settings" cover how the cell looks and what it is watching. Size the buttons, set their text size, borders, edges and gradients, zoom the whole cell, and choose whether values carry decimals or read as whole numbers. The same panel is where you add and remove the values themselves, widening a row with another feed or stacking a new row beneath it.

*Note: Removing a feed or a row parks it rather than deleting it. The next feed or row you add brings back the most recently removed one, with its source, label and colours intact, so a layout experiment costs you nothing to undo.*

##### Close Monitor
Closes the Monitor Cell. Your feeds, labels and colours are kept, so reopening it brings everything back exactly as it was.

##### Monitor Button
A "Monitor Button" displays one live number and the label you give it. It can be pointed at any numeric value in any feed you have connected: account balance, open profit and loss, cash on hand, position size, the day's realised total, or anything else your platform exports.

Choosing what it shows takes a right-click. The button opens its own picker, where you select the feed and then the value inside it, and it begins updating straight away. If a feed carries only one usable number, RiskCells selects it for you and stays out of the way. You can repoint a button at a different feed or a different value at any time, without opening settings at all.

The label is yours to set. Platforms name their columns their own way, and those names are rarely the ones you would choose, so double-click any button and rename it to whatever you actually call that number.

Colour is where the cell earns its place on screen. A button can hold one fixed colour, or it can change with the sign of its value: one look when you are up, another when you are down, and your neutral colour at exactly zero, so a closed position returns instantly to its resting state. Background, text and border are each independently colourable in every state, which means you can make a number shout or let it sit quietly in the background until it matters.

A Monitor Cell holds up to four values across and five rows deep, twenty in total. Any row can sit inside the cell, float free on your canvas, or tuck into the control bar as compact pills when you want the value without the footprint (see "Embed Place"). And if you need more than one cell's worth, open another window. Every window carries its own cells, and you can run up to twenty of them.

*Note: Together with the Risk Cell, this closes the loop. Your account balance can be driving your risk automatically while the same balance sits in front of you as a number you can see, so you are never sizing from a figure you have to go and check somewhere else.*

##### Open PNL
"Open PNL" is another user-named button, and it shows why the Monitor Cell is worth having on screen. Values that swing between positive and negative can be coloured by their sign: one palette when you are up, another when you are down, and your neutral colour at exactly zero, so closing a position returns the tile to its resting state instantly. Background, text and border are each independently colourable in all three states.

The result is a readout you interpret without reading. A glance tells you where you stand before you have processed a single digit, which is exactly what you want from a number you check hundreds of times a session.

*Note: Sign colouring is off by default, so every value starts on a single colour until you decide it should change with its sign.*

##### Embed Place
A row of Monitor values can live in three places, and you move it between them by dragging. It can sit inside the cell as a normal row, float free on your canvas as its own small panel positioned anywhere you like, or embed itself directly into the cell's control bar as a strip of compact pills.

Embedding is for the values you always want visible but never want in the way. The pills shrink to fit their content and tuck into the bar itself, staying completely live while taking almost no space. Drag a floating row over the control bar and it highlights to show it will take it; drop it and it embeds. Drag it back out and it becomes a floating panel again, right where you pulled it from.

*Note: An embedded value updates exactly like a full-size one. Nothing is paused or simplified by embedding it, only made smaller.*

## Onboarding

---

### NinjaTrader

#### PART 1: INSTALL RISKCELLS

1. Download RiskCells. Use the download link in your welcome email, or go to riskcells.com,
   open Resources and choose Download Software. The file is called RiskCells-Setup.exe.

2. Double-click RiskCells-Setup.exe.
   - If Windows shows "Windows protected your PC", click More info, then Run anyway.
   - If Windows asks for permission to make changes, click Yes.

3. Follow the installer.

4. Open RiskCells from the desktop shortcut or the Start menu.

#### PART 2: SIGN IN

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

#### PART 3: CONNECTING YOUR PLATFORM: NINJATRADER

1. On riskcells.com, open Resources and choose Download NinjaTrader Bundle. The file is
   called RiskCells-NinjaTrader-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside are four zip files, one for each
   indicator. Do not unzip these four: NinjaTrader imports them as zip files.
   - RiskCellsTicksFromMouseV5_NT.zip   (Mouse Ticks)
   - RiskCellsAtrFeed_NT.zip            (Hourly ATR)
   - RiskCellsAtrFeedDaily_NT.zip       (Daily ATR)
   - RiskCellsAccountLink_NT.zip        (Account Link)

#### PART 4: IMPORT THE INDICATORS INTO NINJATRADER

1. In the NinjaTrader Control Center, go to Tools > Import > NinjaScript Add-On.

2. Select RiskCellsTicksFromMouseV5_NT.zip and click Import. NinjaTrader tells you when the
   import is complete.

3. Repeat for the other three zip files.

#### PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

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

#### PART 6: ADD THE INDICATORS TO YOUR CHARTS

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

##### MOUSE TICKS

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

##### HOURLY ATR

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

3. In RiskCells, choose the feed (for example ES 1H) in the dropdown above the ATR field,
   then turn on DYN or LOCK (see ATR MODES below).

Tip: leave the contract month out of the name and add the timeframe instead, so the feed
is easy to find later, for example ES 1H.

##### DAILY ATR

1. Open a daily chart of the instrument: in Data Series, set Type to Day and Value to 1,
   then click OK.

2. Add RiskCells™ ATR FEED DAILY (steps A to E above). In its Properties, set:
   - Input series: ATR under Indicators, the same way as for the hourly chart.
   - Instrument base name: for example ES. The indicator adds -D1 for the daily timeframe,
     so the feed shows as ES-D1. If you leave it empty, it uses the chart's symbol.
   - Output folder path: enter your feed folder from Part 5.
   - JSON Write Interval in Milliseconds (default: 250): how often the feed file is updated.

   Click OK.

3. In RiskCells, choose ES-D1 in the dropdown above the ATR field, then turn on DYN or LOCK
   (see ATR MODES below).

##### ACCOUNT LINK

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

##### ATR MODES: DYN, MAX AND LOCK

When an ATR feed is selected, DYN, MAX and LOCK appear on the calculator. The ATR field only
takes the feed's value once DYN or LOCK is on. Until then, its indicator shows the feed as
stopped.

- DYN follows the live ATR and keeps updating.
- LOCK holds one past reading that you pick in the list next to it.<br>
  Hourly feed: pick a time of day (Latest = the last completed hour). If that time has not
  come yet today, yesterday's reading at that time is used.<br>
  Daily feed: pick a day of the week (Previous = the last completed day).
- MAX works together with DYN or LOCK and uses today's highest ATR so far. On an hourly
  feed with LOCK, MAX uses today's highest ATR until your chosen time comes, then the
  reading at that time.

Click DYN or LOCK again to turn it off. While ATR is in use, RiskCells sets Stop / Ticks
from the ATR and the percentage button you choose on the calculator.

##### SAVE YOUR WORKSPACE

When your indicators are in place, save your workspace from the Workspaces menu in the
Control Center, so they are there the next time you open NinjaTrader. NinjaTrader also asks
whether to save when you close it.

#### PART 7: SMOOTHER UPDATES (OPTIONAL)

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

##### WARNING

- Faster updates cost CPU in both NinjaTrader and RiskCells.
- Very fast poll rates also make RiskCells work harder, especially with many feeds and
  windows open.
- If NinjaTrader or your PC starts to lag, raise the numbers again, for example to 100.

#### PART 8: CHECK THAT EVERYTHING WORKS

- The readout on your NinjaTrader chart changes as you move the mouse.
- In RiskCells, the dots beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in RiskCells once DYN or LOCK is on.
- Your account value shows in the live mode in Risk Parameters.

##### HOW TO READ THE LIVE / STALE INDICATORS

RiskCells shows the state of every feed with a coloured dot. Each feed dropdown on a
calculator has its own dot, and each row has a master dot next to the row name.

Feed dot:
- Blue: the feed is updating.
- Pink: no update for about 8 seconds, or the feed has no usable value (for example an ATR
  feed without DYN or LOCK). The last value stays in the field.
- Grey: MANUAL, no feed selected.

Master dot, for all the feeds selected in that row:
- Blue: every selected feed is updating. It is also blue when no feed is selected.
- Yellow: at least one feed has stopped while others are updating. Look for the pink dot in
  that row.
- Pink: none of the selected feeds are updating.

These are the default colours. You can change them in Master Settings > Graphic Settings.

#### TROUBLESHOOTING

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

---

### Quantower

#### PART 1: INSTALL RISKCELLS

1. Download RiskCells. Use the download link in your welcome email, or go to riskcells.com,
   open Resources and choose Download Software. The file is called RiskCells-Setup.exe.

2. Double-click RiskCells-Setup.exe.
   - If Windows shows "Windows protected your PC", click More info, then Run anyway.
   - If Windows asks for permission to make changes, click Yes.

3. Follow the installer.

4. Open RiskCells from the desktop shortcut or the Start menu.

#### PART 2: SIGN IN

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

#### PART 3: CONNECTING YOUR PLATFORM: QUANTOWER

1. On riskcells.com, open Resources and choose Download Quantower Bundle. The file is
   called RiskCells-Quantower-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside are four files:
   - RiskCellsTicksFromMouse_QT.dll   (Mouse Ticks)
   - RiskCellsAtrFeed_QT.dll          (Hourly ATR)
   - RiskCellsAtrFeedDaily_QT.dll     (Daily ATR)
   - RiskCellsAccountLink_QT.dll      (Account Link)

#### PART 4: COPY THE INDICATORS INTO QUANTOWER

1. Close Quantower.

2. Open the folder you installed Quantower in, then go to Settings\Scripts\Indicators.

3. Copy the four DLL files into that folder.

4. Open Quantower. If the indicators are not listed, create a folder called RiskCells
   inside Settings\Scripts\Indicators, move the four DLL files into it and restart
   Quantower again.

#### PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

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

#### PART 6: ADD THE INDICATORS TO YOUR CHARTS

How to add a RiskCells indicator to a chart. Do this for each indicator, on every chart you
want to send data to RiskCells from:

- A. Open the indicators window from the sidebar on the chart.
- B. Type RiskCells in the search bar.
- C. Double-click the indicator. It is added to the chart and its settings window opens.
- D. Set the settings described below.
- E. When the settings are done, click OK.

This is how the indicators are named in the indicators window:

| Indicator | Name in the list |
|---|---|
| Mouse Ticks | RiskCells™ MouseTicksControl |
| Hourly ATR | RiskCells™ ATR Feed |
| Daily ATR | RiskCells™ ATR Feed Daily |
| Account Link | RiskCells™ ACCOUNT LINK |

##### MOUSE TICKS

1. Open a chart of the instrument you trade. Any timeframe works.

2. Add RiskCells™ MouseTicksControl (steps A to E above). Its settings, in the order you
   see them:

   - Current Price Source (default: Bid)<br>
     The live price the distance is measured from: Bid, Ask or Last Trade.

   - Chart Compression Factor (default: 1)<br>
     Made for compressed charts on instruments with big ranges, such as NQ. The indicator
     measures the distance in the chart's tick size and divides it by this number. Leave it
     at 1 if the chart does not use a custom tick size. If it does, enter the instrument's
     real tick size divided by the chart's tick size, so RiskCells still gets the real tick
     count your risk is calculated from.

   - Round Output (default: unticked)<br>
     Unticked sends the value with two decimals. Ticked sends whole ticks.

   - File name prefix (default: ES 1)<br>
     The name of this feed in RiskCells, for example ES TICKS. The feed file gets exactly
     this name.

   - JSON Write Interval in Milliseconds (default: 100)<br>
     The shortest time between two updates of the feed file. 0 writes as fast as
     practical, about every 25 ms. Lower is smoother but uses more CPU (see Part 7).

   - Output folder path<br>
     The folder the feed file is written to. Enter your feed folder from Part 5, for
     example C:\RiskCells Feeds. If you leave it empty, the file goes into Quantower's own
     folder, which RiskCells does not watch.

   - Multi-Chart Mouse Handoff (default: ticked)<br>
     Made so one feed can follow your mouse across several charts. Ticked: when charts
     share the same File name prefix, only the chart under your mouse sends its value.
     Unticked: this chart always sends, so only untick it when each chart has its own name.

   - Show readout on chart (default: ticked)<br>
     Shows the distance in ticks on the chart.

   - Readout corner (default: Top Left)<br>
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
- The feed file is created the first time you move your mouse over the chart's main price
  panel, as long as Quantower is connected and receiving live prices.
- Only the main price panel counts. Moving over a panel below it keeps the last value.
- Using several charts? Add the indicator to each chart with the same File name prefix.
  Only the chart under your mouse sends its value, so RiskCells follows the chart you
  point at.

##### HOURLY ATR

1. Open a chart of the instrument. Any timeframe works: the indicator loads its own 1-hour
   bars. Use a chart without a custom tick size, because the indicator sends the chart's
   tick size and RiskCells uses it to turn the ATR into ticks.

2. Add RiskCells™ ATR Feed (steps A to E above). Its settings, in the order you see them:

   - Instrument name (default: empty)<br>
     The name RiskCells shows for this feed, for example ES 1H. If you leave it empty, it
     uses the chart's symbol name.

   - ATR Period (default: 14)<br>
     The number of hourly bars in the ATR.

   - ATR Smoothing (default: Simple (SMA))<br>
     How the true ranges are averaged: Simple (SMA), Wilder (SMMA) or Exponential (EMA).

   - New trading day starts at hour (default: 0)<br>
     The hour, in the display time zone, when today's hours start again. 0 is midnight.
     For a session that opens in the evening, enter its opening hour, for example 18.

   - Display Time Zone id (default: empty)<br>
     The time zone for the hour labels and the day split, as a Windows time zone name such
     as Eastern Standard Time. Empty uses your PC's time zone.

   - History lookback (days) (default: 10)<br>
     How many days of hourly bars the indicator loads.

   - JSON Write Interval in Milliseconds (default: 250)<br>
     How often the feed file is updated.

   - Output folder path<br>
     Enter your feed folder from Part 5.

   - Show readout on chart (default: ticked)<br>
     Shows the live ATR and today's highest ATR on the chart.

   Note: the Quantower indicators calculate the ATR themselves, so you don't add a separate
   ATR indicator. Set ATR Period and ATR Smoothing to match the ATR you normally use.

3. In RiskCells, choose the feed (for example ES 1H) in the dropdown above the ATR field,
   then turn on DYN or LOCK (see ATR MODES below).

Tip: leave the contract month out of the name and add the timeframe instead, so the feed
is easy to find later, for example ES 1H.

##### DAILY ATR

1. Open a chart of the instrument. Any timeframe works: the indicator loads its own daily
   bars. Use a chart without a custom tick size, as for the hourly ATR.

2. Add RiskCells™ ATR Feed Daily (steps A to E above). Its settings, in the order you see
   them:

   - Instrument base name (default: empty)<br>
     For example ES. The indicator adds -D1 for the daily timeframe, so the feed shows as
     ES-D1. If you leave it empty, it uses the chart's symbol name.

   - ATR Period (default: 14)<br>
     The number of daily bars in the ATR.

   - ATR Smoothing (default: Simple (SMA))<br>
     How the true ranges are averaged, as for the hourly ATR.

   - Days to include (default: 5)<br>
     How many completed days the feed sends. LOCK picks from these days.

   - Daily date from (default: Session close)<br>
     Which end of the daily bar gives it its date. Keep Session close. Switch to Session
     open if your dates come out one day early.

   - Display Time Zone id (default: empty)<br>
     The time zone for the day split, as for the hourly ATR.

   - History lookback (days) (default: 250)<br>
     How many days of daily bars the indicator loads.

   - JSON Write Interval in Milliseconds (default: 250)<br>
     How often the feed file is updated.

   - Output folder path<br>
     Enter your feed folder from Part 5.

   - Show readout on chart (default: ticked)<br>
     Shows today's ATR and today's highest ATR on the chart.

3. In RiskCells, choose ES-D1 in the dropdown above the ATR field, then turn on DYN or LOCK
   (see ATR MODES below).

##### ACCOUNT LINK

Account Link sends your Quantower account values, such as your balance, to RiskCells. The
live risk modes in Risk Parameters use them to size from your real balance, and Monitor
Cells can show them.

1. Open any chart. Account Link needs a chart to run on, but the instrument does not matter.
   Add it to one chart only.

2. Add RiskCells™ ACCOUNT LINK (steps A to E above). Its settings, in the order you see
   them:

   - Account<br>
     The account to send.

   - Write all connected accounts (instead of the selected one) (default: unticked)<br>
     Ticked sends one feed for every connected account instead.

   - Write combined file (all-accounts mode only) (default: unticked)<br>
     With all accounts ticked, also sends one extra feed that adds all accounts together.

   - Output folder path<br>
     Enter your feed folder from Part 5.

   - Write Interval in Milliseconds (minimum 10) (default: 10)<br>
     How often the account feed is updated. It also updates straight away when a position
     opens or closes.

   - Per-account file name prefix (default: empty)<br>
     Text placed in front of the account name in the feed name. Empty names each feed
     after its account.

   - Combined file name (without .json) (default: combined)<br>
     The name of the combined feed.

   - INCLUDE POSITIONS ARRAY (default: ticked)<br>
     Adds a detailed list of your open positions to the feed. Your balance and profit and
     loss values are sent either way.

3. In RiskCells, open Master Settings > Risk Parameters and click the live mode you use:
   DTDS Live, ACC % Live or KELLY Live. Fill in its settings, choose your account in its
   Feed dropdown, then choose the value to size from in the list next to it, for example
   Account Balance.<br>
   Note: until you choose a value, RiskCells uses the first one in alphabetical order,
   which is usually not your balance. Some connections report the balance under another
   value, for example one of the Acc values, so check that the number matches your balance.

4. On each calculator that should use it, choose the same account in the dropdown above
   Risk. Risk per trade then comes from the live mode.<br>
   Note: if that account is not the Feed of the live mode that is on, Risk takes the plain
   value chosen next to the dropdown instead, for example your whole balance.

5. To show an account value in a Monitor Cell, right-click a Monitor button and choose the
   account, then the value.

##### ATR MODES: DYN, MAX AND LOCK

When an ATR feed is selected, DYN, MAX and LOCK appear on the calculator. The ATR field only
takes the feed's value once DYN or LOCK is on. Until then, its indicator shows the feed as
stopped.

- DYN follows the live ATR and keeps updating.
- LOCK holds one past reading that you pick in the list next to it.<br>
  Hourly feed: pick a time of day (Latest = the last completed hour). If that time has not
  come yet today, yesterday's reading at that time is used.<br>
  Daily feed: pick a day of the week (Previous = the last completed day).
- MAX works together with DYN or LOCK and uses today's highest ATR so far. On an hourly
  feed with LOCK, MAX uses today's highest ATR until your chosen time comes, then the
  reading at that time.

Click DYN or LOCK again to turn it off. While ATR is in use, RiskCells sets Stop / Ticks
from the ATR and the percentage button you choose on the calculator.

##### SAVE YOUR WORKSPACE

Quantower saves your workspace automatically every five minutes and when you close it. To
save it straight away, press Ctrl + S.

#### PART 7: SMOOTHER UPDATES (OPTIONAL)

The Mouse Ticks indicator writes its feed every 100 ms, and RiskCells reads Stop / Ticks and
ATR feeds every 100 ms by default. For a smoother Stop / Ticks value you can make both
faster. Faster updates use more CPU, so read the warning below first.

In Quantower, on each chart that has the Mouse Ticks indicator:

1. Open the indicator's settings again, for example through the object manager in the
   chart's sidebar. Set "JSON Write Interval in Milliseconds" to 0, so it writes as fast as
   practical (about every 25 ms). Click OK.

The indicator writes on its own timer, so there is no Quantower chart setting to change.
ATR changes slowly, so your ATR indicators can stay as they are.

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

##### WARNING

- Faster updates cost CPU in both Quantower and RiskCells.
- Very fast poll rates also make RiskCells work harder, especially with many feeds and
  windows open.
- If Quantower or your PC starts to lag, raise the numbers again, for example to 100.

#### PART 8: CHECK THAT EVERYTHING WORKS

- The readout on your Quantower chart changes as you move the mouse.
- In RiskCells, the dots beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in RiskCells once DYN or LOCK is on.
- Your account value shows in the live mode in Risk Parameters.

##### HOW TO READ THE LIVE / STALE INDICATORS

RiskCells shows the state of every feed with a coloured dot. Each feed dropdown on a
calculator has its own dot, and each row has a master dot next to the row name.

Feed dot:
- Blue: the feed is updating.
- Pink: no update for about 8 seconds, or the feed has no usable value (for example an ATR
  feed without DYN or LOCK). The last value stays in the field.
- Grey: MANUAL, no feed selected.

Master dot, for all the feeds selected in that row:
- Blue: every selected feed is updating. It is also blue when no feed is selected.
- Yellow: at least one feed has stopped while others are updating. Look for the pink dot in
  that row.
- Pink: none of the selected feeds are updating.

These are the default colours. You can change them in Master Settings > Graphic Settings.

#### TROUBLESHOOTING

**The indicators are not in the indicators window**
- Check that the four DLL files are in Settings\Scripts\Indicators inside your Quantower
  folder, then restart Quantower.
- Still missing? Create a folder called RiskCells inside Settings\Scripts\Indicators, move
  the four DLL files into it and restart Quantower again.
- Make sure you extracted the DLL files from the zip file. Quantower can't use them while
  they are still inside the zip.
- Type RiskCells in the search bar of the indicators window.

**A feed is missing from the RiskCells dropdown**
- Mouse Ticks: move your mouse over the chart's main price panel. The file is created on
  the first movement, and Quantower must be connected and receiving live prices.
- Hourly and Daily ATR: the indicators load price history first, so the first update can
  take a few seconds. Quantower must be connected.
- Account Link: choose an Account in its settings, or tick Write all connected accounts.
  Quantower must be connected.
- Check that the folder in the indicator's Output folder path is listed in Feed Folders and
  switched on.
- A typo in the Output folder path does not show an error: the indicator creates a new
  folder with the mistyped name and writes the feed there, where RiskCells does not look.
  Copy the exact path from the address bar of your feed folder in File Explorer and paste
  it into the setting.
- Look for the name you gave the indicator: its File name prefix (Mouse Ticks), its
  Instrument name or the chart's symbol (Hourly ATR), its base name with -D1 added (Daily
  ATR), or the account name with any prefix (Account Link).

**Stop / Ticks does not follow my mouse**
- Move your mouse over the main price panel of the chart that has the indicator.
- If the calculator's ATR field has a value, Stop / Ticks is worked out from the ATR
  instead. Turn ATR off on that calculator with its ATR button.
- Using the same File name prefix on several charts and you closed the chart that was
  sending? Move your mouse over another chart with that name. It takes over within a few
  seconds.

**A feed dot is pink**
- RiskCells has had no update from that indicator for about 8 seconds. Check that
  Quantower is open and connected, and the indicator is still on the chart.
- For an ATR feed, check that DYN or LOCK is on.

**ATR shows 0 or looks wrong**
- Check that DYN or LOCK is on.
- Check that ATR Period and ATR Smoothing match the ATR you normally use.
- Check that the chart does not use a custom tick size.

**Account value shows 0**
- In Risk Parameters, choose the value in the list next to the live mode's Feed dropdown.
  Until you do, RiskCells uses the first value alphabetically.
- Some connections report the balance under another value. Try the Acc values in the list.

Need help? Email info@riskcells.com.

---

### Sierra Chart

#### PART 1: INSTALL RISKCELLS

1. Download RiskCells. Use the download link in your welcome email, or go to riskcells.com,
   open Resources and choose Download Software. The file is called RiskCells-Setup.exe.

2. Double-click RiskCells-Setup.exe.
   - If Windows shows "Windows protected your PC", click More info, then Run anyway.
   - If Windows asks for permission to make changes, click Yes.

3. Follow the installer.

4. Open RiskCells from the desktop shortcut or the Start menu.

#### PART 2: SIGN IN

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

#### PART 3: CONNECTING YOUR PLATFORM: SIERRA CHART

1. On riskcells.com, open Resources and choose Download Sierra Chart Bundle. The file is
   called RiskCells-SierraChart-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside are three files:
   - RiskCellsTicksFromMouse_SC.dll   (Mouse Ticks)
   - RiskCellsAtrFeed_SC.dll          (Hourly ATR)
   - RiskCellsAtrFeedDaily_SC.dll     (Daily ATR)

#### PART 4: COPY THE STUDIES INTO SIERRA CHART

1. Open the file path where your Sierra Chart is installed and navigate to the "Data" folder.
   Usually the path is: C:\SierraChart\Data

2. Copy the three DLL files into that folder.

3. Running more than one Sierra Chart instance? Copy the files into the Data folder of your
   main instance, then restart Sierra Chart so the studies appear in your other instances.

#### PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

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

#### PART 6: ADD THE STUDIES TO YOUR CHARTS

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

##### MOUSE TICKS

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

##### HOURLY ATR

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

4. In RiskCells, choose the feed (for example ES 1H) in the dropdown above the ATR field,
   then turn on DYN or LOCK (see ATR MODES below).

Tip: leave the contract month out of the name and add the timeframe instead, so the feed
is easy to find later, for example ES 1H.

##### DAILY ATR

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

4. In RiskCells, choose ES-D1 in the dropdown above the ATR field, then turn on DYN or LOCK
   (see ATR MODES below).

##### ATR MODES: DYN, MAX AND LOCK

When an ATR feed is selected, DYN, MAX and LOCK appear on the calculator. The ATR field only
takes the feed's value once DYN or LOCK is on. Until then, its indicator shows the feed as
stopped.

- DYN follows the live ATR and keeps updating.
- LOCK holds one past reading that you pick in the list next to it.<br>
  Hourly feed: pick a time of day (Latest = the last completed hour). If that time has not
  come yet today, yesterday's reading at that time is used.<br>
  Daily feed: pick a day of the week (Previous = the last completed day).
- MAX works together with DYN or LOCK and uses today's highest ATR so far. On an hourly
  feed with LOCK, MAX uses today's highest ATR until your chosen time comes, then the
  reading at that time.

Click DYN or LOCK again to turn it off. While ATR is in use, RiskCells sets Stop / Ticks
from the ATR and the percentage button you choose on the calculator.

##### SAVE YOUR CHARTBOOK

When your studies are in place, choose File > Save in Sierra Chart so they are there the
next time you open it.

#### PART 7: SMOOTHER UPDATES (OPTIONAL)

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

##### WARNING

- Faster updates cost CPU in both Sierra Chart and RiskCells.
- Sierra Chart does not recommend chart update intervals below 100 ms, and asks users not
  to contact its support about problems caused by very short intervals.
- Use short intervals only on the charts that need them, never in Sierra Chart's global
  settings.
- Very fast poll rates also make RiskCells work harder, especially with many feeds and
  windows open.
- If Sierra Chart or your PC starts to lag, raise the numbers again, for example to 100.

#### PART 8: CHECK THAT EVERYTHING WORKS

- "Ticks Away" at the top of your Sierra Chart chart changes as you move the mouse.
- In RiskCells, the indicators beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in RiskCells once DYN or LOCK is on.

##### HOW TO READ THE INDICATORS

Each feed dropdown has its own indicator, and each row has a master indicator next to the
row name.

Feed indicator:
- Blue: the feed is updating.
- Pink: no update for about 8 seconds, or the feed has no usable value (for example an ATR
  feed without DYN or LOCK). The last value stays in the field.
- Grey: MANUAL, no feed selected.

Master indicator, for all the feeds selected in that row:
- Blue: every selected feed is updating. It is also blue when no feed is selected.
- Yellow: at least one feed has stopped while others are updating. Look for the pink
  indicator in that row.
- Pink: none of the selected feeds are updating.

These are the default colours. You can change them in Master Settings > Graphic Settings.

#### TROUBLESHOOTING

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

---

### TradingView

#### BEFORE YOU START: THE TRADINGVIEW BRIDGE IS A BETA

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

#### PART 1: INSTALL RISKCELLS

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

#### PART 2: SIGN IN

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

#### PART 3: CONNECTING YOUR PLATFORM: TRADINGVIEW

1. On riskcells.com, open Resources and choose Download TradingView Bundle. The file is
   called RiskCells-TradingView-Bundle.zip.

2. Right-click the zip file and choose Extract All. Inside is a folder called
   RiskCells-TV-Bridge with the extension's files, including manifest.json.

3. Move the RiskCells-TV-Bridge folder to a place where it can stay, for example your
   Documents folder. Your browser runs the extension from this folder, so don't delete,
   move or rename it after Part 4.

#### PART 4: ADD THE EXTENSION TO YOUR BROWSER

The bridge is not in the Chrome Web Store, so you add it with your browser's Developer
mode. Use the browser you open TradingView in.

##### GOOGLE CHROME

1. Type chrome://extensions in the address bar and press Enter.

2. Switch on Developer mode.

3. Click Load unpacked.

4. Choose the RiskCells-TV-Bridge folder, the one with manifest.json directly inside it,
   and click Select Folder. RiskCells TV Bridge (BETA) now shows on the page.

5. Pin it to the toolbar: click the Extensions button next to the address bar, then click
   the pin next to RiskCells TV Bridge (BETA).

##### MICROSOFT EDGE

1. Click Settings and more (...), then Extensions, then Manage extensions.

2. Switch on Developer mode.

3. Click Load unpacked, choose the RiskCells-TV-Bridge folder and click Select Folder.

4. Click the Extensions button next to the address bar, then click RiskCells TV Bridge
   (BETA). Its icon is added next to the address bar.

##### VIVALDI

Follow steps 1 to 4 for Google Chrome, but type vivaldi://extensions in step 1.

From now on your browser may warn you about extensions in developer mode, for example when
it starts. Keep RiskCells TV Bridge switched on.

#### PART 5: PREPARE RISKCELLS: YOUR FEED FOLDER

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

#### PART 6: CONNECT YOUR TRADINGVIEW CHARTS

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

##### MOUSE TICKS

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

##### HOURLY ATR

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

##### DAILY ATR

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

##### ACCOUNT VALUES

The bridge sends chart values and your mouse position only. It does not send account
values such as your balance, so there is no Account Link for TradingView. The live risk
modes in Risk Parameters (DTDS Live, ACC % Live and KELLY Live) need an account feed, so
with TradingView alone you set your risk on the calculators yourself.

##### ATR MODES: DYN, MAX AND LOCK

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

##### SAVE YOUR LAYOUT

- Save your TradingView layout with Ctrl + S, or switch on Autosave in the layout menu.
- The bridge remembers your feeds in your browser. After you restart the browser, open the
  same charts again: each feed reconnects by itself to a chart that shows the same symbol
  in the same place of the same layout.
- A feed whose chart is not open is listed under Remembered feeds not on screen. It
  continues by itself when that chart is open again. You can also drag it onto a chart in
  the panel, or click Apply when a chart with the same symbol is open. Forget removes it.

##### UPDATING THE BRIDGE

The bridge does not update by itself. When a new version comes out:

1. Download RiskCells-TradingView-Bundle.zip again and extract it (Part 3).

2. Replace your RiskCells-TV-Bridge folder with the new one, in the same place.

3. Open your browser's extensions page (Part 4) and reload RiskCells TV Bridge (BETA): in
   Chrome and Vivaldi, click the reload arrow on its card. In Edge, click Reload on its
   card.

4. Reload your TradingView chart tabs with F5.

Your feeds and your FEED FOLDER stay as they are.

#### PART 7: SMOOTHER UPDATES (OPTIONAL)

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

##### WARNING

- Very fast poll rates make RiskCells work harder, especially with many feeds and windows
  open.
- If RiskCells or your PC starts to lag, raise the numbers again, for example to 100.

#### PART 8: CHECK THAT EVERYTHING WORKS

- The TV Bridge panel says STATUS: LIVE.
- Every row you switched on shows writing, and its number keeps going up. When several
  charts share one Mouse name, the charts you are not pointing at show standby.
- The bridge's toolbar icon shows the number of feeds being written, on a blue badge.
- In RiskCells, the dots beside your Stop / Ticks and ATR dropdowns are blue.
- On the calculator you use for Mouse Ticks, Stop / Ticks follows your mouse.
- Your ATR value shows in the calculator's ATR field.

##### HOW TO READ THE LIVE / STALE INDICATORS

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

#### TROUBLESHOOTING

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

