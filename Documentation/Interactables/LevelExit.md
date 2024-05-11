# LevelExit
> namespace Gamekit2D.Runtime.Interactables
```csharp
public sealed class LevelExit : InteractiveObject
```
## Summary
Interactable behaviour, changes the scene when the player touches the trigger of the object
this component is on.

## Fields
| Name | Type | Description |
| scene | SceneAsset | Scene to load |
| useAsyncLoading | bool | When true, uses asynchronous loading to load the given scene |
| showLoadingBar | Only applies when useAsyncLoading is enabled. When toggled on, the framework will show the default loading bar while the scene is loading in the background |
