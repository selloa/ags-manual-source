## Change room

Move the player (or another character) into a different room.

### Script

```ags
// Room number only — keep current position style / defaults
player.ChangeRoom(2);

// Place at coordinates, facing a direction
player.ChangeRoom(4, 100, 50, eDirectionRight);
```

Typical edge / door hotspot:

```ags
function hDoor_Interact()
{
    player.ChangeRoom(2, 50, 140);
}
```

### Notes

- The room change is queued and happens when the current script finishes (same idea as dialog start).
- Optional X/Y place the character in the destination room; omit them to use the room’s default entry behavior where applicable.

### See also

- [Character](Character) · [ChangeRoom](Character#characterchangeroom)
- [Room](Room)
