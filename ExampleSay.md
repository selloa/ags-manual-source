## Character speech

Make a character speak a line (speech view / voice if set up).

### Script

```ags
cEgo.Say("My name is Ego.");
```

With formatting:

```ags
cEgo.Say("I have %d keys.", key_count);
```

### Notes

- `Say` is blocking until the line finishes.
- Prefer `player.Say(...)` when you mean the current player character.
- For a narrator message box without a speaking character, use [Display a message](ExampleDisplay).

### See also

- [Character](Character) · [Say](Character#charactersay)
- [Speech](Speech)
- [Understanding blocking scripts](BlockingScripts)
