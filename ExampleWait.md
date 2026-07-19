## Wait (blocking)

Pause the current script for a number of game loops while the game continues to animate.

### Script

```ags
cEgo.Walk(120, 140, eBlock);
Wait(80);  // ~2 seconds at 40 loops/sec
cEgo.Say("Made it.");
```

### Notes

- `Wait` blocks the script thread — other scripts on that thread will not run until it returns.
- Default game speed is 40 loops per second (`80` ≈ 2 seconds) unless you change it.
- For skippable pauses, see `WaitKey`, `WaitMouse`, and related commands on the Wait page.

### See also

- [Global functions: wait](Globalfunctions_Wait) · [Wait](Globalfunctions_Wait#wait)
- [Understanding blocking scripts](BlockingScripts)
