# RiskCells

## Contents

- [About RiskCells](#about-riskcells)
  - [The software](#the-software)
  - [Platforms](#platforms)
  - [Licence & devices](#licence--devices)
  - [Features](#features)
- [Onboarding](#onboarding)
  - [NinjaTrader](NinjaTrader.md)
  - [Quantower](Quantower.md)
  - [Sierra Chart](SierraChart.md)
  - [TradingView](TradingView.md)

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
- [NinjaTrader setup](NinjaTrader.md)
- [Quantower setup](Quantower.md)
- [Sierra Chart setup](SierraChart.md)
- [TradingView setup](TradingView.md)
