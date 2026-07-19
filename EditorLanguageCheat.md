## Language cheat sheet

Essentials for writing AGS Script. For full detail see [Script language keywords](ScriptKeywords).

### Types and values

- Built-ins: `int`, `float`, `bool`, `char`, `String` (capital S)
- Enums and constants: see [Standard Enumerated Types](StandardEnums), [Standard Constants](Constants)
- Structs and managed objects: [Structs](ScriptStructs), [Managed Structs](ScriptManagedStructs), [Pointers](Pointers)
- Arrays: fixed and [dynamic arrays](DynamicArrays)

### Control flow

```ags
if (cond) { ... } else { ... }
while (cond) { ... }
for (i = 0; i < n; i++) { ... }
switch (x) { case 1: ... break; }
```

### Functions and scripts

- Declare with `function name(...)` / `import` in headers
- Share across modules: [Importing functions and variables](ImportingFunctionsAndVariables), [The script header](TheScriptHeader), [Multiple Scripts](MultipleScripts)
- Extend built-in types: [Extender functions](ExtenderFunctions), [OO programming](OOProgramming)
- Dialog scripts use `@` labels: [Dialog Script](DialogScript)

### Blocking vs non-blocking

Many commands (e.g. `Character.Walk`, `Display`) **block** until finished. Non-blocking variants or `eNoBlock` let the game continue. See [Understanding blocking scripts](BlockingScripts).

### Events

- Global handlers: `game_start`, `on_event`, `repeatedly_execute`, … — [Global event handlers](Globalfunctions_Event)
- Object events (room, GUI, …): [Event Types](EventTypes)
- Order of execution: [Game events order](GameEventsOrder)

### Strings and formatting

- Prefer `String` methods; formatting helpers: [String formatting](StringFormats), [String](String)

### Preprocessor

- `#if` / `#define` / version macros: [Preprocessor](Preprocessor)

### See also

- [Script API A–Z index](ScriptAPIIndex)
- [Cheats and quick guides](EditorCheats)
