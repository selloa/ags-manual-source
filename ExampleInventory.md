## Add / remove inventory

Give or take an inventory item from a character.

### Script

```ags
cEgo.AddInventory(iKey);
cEgo.LoseInventory(iKey);
```

Check before using:

```ags
if (cEgo.HasInventory(iKey))
{
    cEgo.LoseInventory(iKey);
    Display("You use the key.");
}
```

### Notes

- Use the inventory item’s **script name** from the editor (`iKey`, not a numeric ID).
- `LoseInventory` removes one quantity; call again if the stack count is higher.

### See also

- [Character](Character) · [AddInventory](Character#characteraddinventory) · [LoseInventory](Character#characterloseinventory)
- [InventoryItem](InventoryItem)
