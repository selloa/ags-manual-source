## Interact with an object

Handle a room object’s event and change its state.

### Script

Look / interact event (name matches the Events pane):

```ags
function oDoor_Interact()
{
    player.FaceObject(oDoor);
    player.Say("It's locked.");
}
```

Hide the object after using an item:

```ags
function oDoor_UseInv()
{
    if (player.ActiveInventory == iKey)
    {
        player.LoseInventory(iKey);
        oDoor.Visible = false;
        Display("The door swings open.");
    }
}
```

### Notes

- Object script names come from the Room Editor (`oDoor`, `oTable`, …).
- Wire the function in the object’s **Events** list so AGS calls it on that interaction.

### See also

- [Object](Object) · [Visible](Object#objectvisible)
- [Character](Character) · [FaceObject](Character#characterfaceobject)
- [Event Types](EventTypes)
- [Add / remove inventory](ExampleInventory)
