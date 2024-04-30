# GamekitSettingsObject
> namespace Gamekit2D.Runtime.Utils
```csharp
public class GamekitSettingsObject : ScriptableObject
```

## Summary
The gamekit settings. Can be edited via Window > Eren's Framework > Framework settings.
Used to control global settings for the gamekit such as scene transitions.

## Fields
| Name | Type                                                   | Description |
|------|--------------------------------------------------------|-------------|
| SceneTransition | [SceneTransition](./../Enums/SceneTransition.md) | Scene transition to use whenever the scene changes |
| TransitionColor | Color | Color of the scene transition to apply |
| SceneTransitionSpeed | float | Speed or duration of the scene transition |
| LoadingWidget | GameObject | The loading widget to use whenever a progress bar is shown. The gameobject selected MUST have a LoadingWidget component attached to it. |