## Script API Overview

AGS provides a scripting system, where engine functionalities are exposed through the AGS Script API, allowing you to write a mini-program, giving you great control over your game. You can read and modify room elements by using the structs [`Room`](Room), [`Object`](Object), [`Hotspot`](Hotspot), [`Region`](Region), and the *Global functions for Room*. If you need your character to *say* things, *receive or lose an inventory item*, or *walk* somewhere, you can find these in the Character struct. The AGS camera system is available through the use of [`Viewport`](Viewport), [`Camera`](Camera), and [`Screen`](Screen). You can also draw directly with [Dynamic Sprites](DynamicSprite), [Drawing Surface](DrawingSurface) and use [Overlays](Overlay) to have these sprites shown on screen.

**NOTE:** API stands for "Application Programming Interface". This is a common term, it defines all the means a program (such as the AGS engine) provides for the user to control it programmatically.

For a full grouped list see [Scripting API](Scripting). To look up a type or topic by name, use the [Script API A-Z index](ScriptAPIIndex). For removed or renamed commands, see [Obsolete Script API](ObsoleteScriptAPI).

### API map

#### Basics

Constants, enumerated types, built-in types, game variables, and global arrays.

See: [Scripting API - Basics](Scripting#basics), [Standard Constants](Constants), [Standard Types](StandardTypes), [Game variables](Gamevariables)

#### Events

Global event handlers, `repeatedly_execute`, save validation, and custom dialog options rendering.

See: [Scripting API - Events](Scripting#events), [Global event handlers](Globalfunctions_Event), [Event Types](EventTypes)

#### Global functions

Standalone commands for messages, waiting, rooms, screen effects, palette, and legacy multimedia.

See: [Scripting API - Global functions](Scripting#global-functions), [Global functions: general](Globalfunctions_General)

#### World

Rooms, characters, hotspots, objects, regions, inventory items, camera, viewport, and screen.

See: [Scripting API - World](Scripting#world), [Character](Character), [Room](Room), [Camera](Camera)

#### UI

Dialogs, GUIs and controls, mouse input, overlays, and text-window GUIs.

See: [Scripting API - UI](Scripting#ui), [GUI](GUI), [Dialog](Dialog), [Mouse](Mouse)

#### Media

Audio channels and clips, drawing surfaces, dynamic sprites, speech, and view frames. Start with [Audio in script](AudioInScript) if you need how playback works.

See: [Scripting API - Media](Scripting#media), [AudioClip](AudioClip), [DrawingSurface](DrawingSurface)

#### Data and system

Files, dictionaries and sets, strings, maths, parser, game/system info, and utilities.

See: [Scripting API - Data and system](Scripting#data-and-system), [File](File), [String](String), [System](System)

### API switches

When a new version of AGS is released and comes with new API entries for additional functionality these changes can possibly cause conflicts with previously made scripts. Sometimes a function gets deprecated (outdated) and disabled, or replaced by a different and better one. Sometimes a new function is added that uses a descriptive name which you already used in your script, which can obviously lead to conflicts. Usually it's a good idea to adjust your script and resolve these problems by hand. But if you do not want to or do not have the time to do so just yet - there are API switches.

In a nutshell, API switches let you control which parts of the API are active in your game.

In the editor the API switches are found in the [General Settings](GeneralSettings), in the "Backwards Compatibility" category. The relevant settings are:

* **Script API version** - defines the *topmost level* of the API. Default is the "Highest" level, which uses the topmost supported API by this version of AGS. Setting it to any version will lock the API at that level, disabling any additions (functions and properties) that were introduced to AGS Script later.
* **Script compatibility level** - defines the *lowest level* of the API. Default is the "Highest" level, which again uses only functionality officially supported by the current version of AGS. Setting it to a lower version enables older functions that now are deprecated.
* **Enforce post-2.62 scripting** - this is on by default, turning this off brings back a huge number of obsolete global functions from the era before AGS 2.7. Most of these functions were replaced by the introduction of [object structs](ScriptKeywords#struct) and properties. See [Upgrading to AGS 2.7](UpgradingTo27) for more information.
* **Enforce new style strings** - this is on by default, turning this off reactivates old-style string functions and also the deprecated `string` type (the contemporary type is `String` with [capital S](String)) which was used differently and had a 200 character limit.
* **Enforce new-style audio scripting** - this is on by default, turning this off reactivates the old-style audio functions that are deprecated since AGS 3.2. These functions rely on passing clip numbers instead of using their script names (which can be chosen freely and are based on the filename), and support strictly 1 channel per audio type. See [Upgrading to AGS 3.2](UpgradeTo32) for more information.
* **Use old-style custom dialog options API** - this is off by default, and enabling this switches to pre-AGS 3.4.0 custom dialog option callbacks. See [Upgrading to AGS 3.4](UpgradeTo34) for more information.
* **Use old-style keyboard handling** - this is off by default, and enabling this switches to old-style key input handling style. See [Upgrading to AGS 3.6](UpgradeTo36#changes-to-key-input-handling) for more information.

Each of the above switches defines a macro or a number of macros which are then used during script compilation and help detect the state of these switches. You can also use these in your script, for example if you want to provide two or more variants of code for different API versions. For more information on this and actual script examples see [Constants](Constants).
