# BackgroundMusicController
> namespace Gamekit2D.Runtime.Audio
```csharp
public sealed class BackgroundMusicController : Singleton<BackgroundMusicController>
```

## Summary
A component that allows easy control over background music in games and across scenes. Attached to the Systems
GameObject that is loaded during initialisation.

## Fields
| Name | Type                            | Description |
|------|---------------------------------|-------------|
| Music | [ThemeMusic](./ThemeMusic.md)[] | Collection of theme songs by scene and clip |