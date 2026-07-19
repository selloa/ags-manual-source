## Play a sound

Play an audio clip from the project’s Audio folder.

### Script

```ags
aDoorSlam.Play();
```

Keep the channel to adjust volume or stop later:

```ags
AudioChannel* chan = aMusicTheme.Play();
if (chan != null)
{
    chan.Volume = 40;
}
```

### Notes

- Playback uses a fixed pool of audio channels; see [Audio in script](AudioInScript) if sounds cut each other off.
- Clip script names come from the editor (`aDoorSlam`, `aMusicTheme`, …).

### See also

- [AudioClip](AudioClip) · [Play](AudioClip#audioclipplay)
- [AudioChannel](AudioChannel)
- [Audio in script](AudioInScript)
