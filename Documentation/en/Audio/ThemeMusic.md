# ThemeMusic
> namespace Gamekit2D.Runtime.Audio.BackgroundMusicController
```csharp
[System.Serializable]
private struct ThemeMusic
```

## Summary
A struct that allows you to customise the background music behaviour and tie it in with specific scenes.

## Fields
| Name | Type | Description |
|------|------|-------------|
| scene | Scene | Scene which the chosen song plays in |
| overrite | bool | When true, the new scene will stop any music from the old song. When false, the new clip will play after the one from the old scene is finished |
| theme | List<AudioClip> | List of theme music or background music. These will play sequentially when the selected scene is active |
