## Walk to a point

Move a character to room coordinates while playing their walking animation.

### Script

```ags
// Non-blocking (default) — script continues while they walk
cEgo.Walk(160, 100);

// Blocking — wait until they arrive
cEgo.Walk(160, 100, eBlock);
```

Ignore walkable areas and walk straight:

```ags
cEgo.Walk(160, 100, eBlock, eAnywhere);
```

### Notes

- Coordinates are **room** space (Room Editor mouse position), not screen pixels.
- Default blocking style is `eNoBlock`; pass `eBlock` when the next line must run after arrival.
- Use [`Character.Move`](Character#charactermove) if you need motion without the walk animation.

### See also

- [Character](Character) · [Walk](Character#characterwalk)
- [Understanding blocking scripts](BlockingScripts)
