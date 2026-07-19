## Display a message

Show a centered message box (common in Look / Interact events).

### Script

```ags
function hSign_Look()
{
    Display("The sign is weathered and hard to read.");
}
```

With a variable:

```ags
Display("You have %d coins.", coins);
```

### Notes

- `Display` is blocking — the script waits until the player dismisses the box.
- Use [`Character.Say`](Character#charactersay) when a character should speak instead of a narrator box.

### See also

- [Global functions: message display](Globalfunctions_Message) · [Display](Globalfunctions_Message#display)
- [String formatting](StringFormats)
- [Character speech](ExampleSay)
