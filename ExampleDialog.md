## Start a dialog

Run a conversation topic created in the Dialog Editor.

### Script

```ags
function cMerchant_Talk()
{
    dMerchant.Start();
}
```

### Notes

- The dialog does **not** start instantly — it runs when the current script function finishes.
- Use the dialog’s script name (`dMerchant`, `dIntro`, …) as set in the editor.

### See also

- [Dialog](Dialog) · [Start](Dialog#dialogstart)
- [Dialog Script](DialogScript)
