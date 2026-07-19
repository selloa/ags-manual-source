## Show / hide a GUI

Toggle a GUI’s visibility from script.

### Script

```ags
gInventory.Visible = true;
gInventory.Visible = false;
```

Toggle:

```ags
gInventory.Visible = !gInventory.Visible;
```

### Notes

- For **Normal** / **Persistent** GUIs, `Visible` simply shows or hides the interface.
- **Popup modal** GUIs pause the game while visible.
- **Mouse Ypos** GUIs: `Visible` controls whether the GUI *may* pop up; use [`GUI.Shown`](GUI#guishown) to see if it is on screen.

### See also

- [GUI](GUI) · [Visible](GUI#guivisible)
- [GUI Editor](EditorGUI)
