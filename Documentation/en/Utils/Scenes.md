# Scenes
> namespace Gamekit2D.Runtime.Utils
```csharp
public sealed class Scenes : Singleton<Scenes>
```

## Summary
A better alternative to the UnityEngine.SceneManagement.SceneManager.
Has more functionality including the option to show a loading bar and built-in scene transitions.
Configure scene transition and loading widget style for the [GamekitSettings](./GamekitSettingsObject.md)

## Methods
### LoadScene(string sceneName)
Loads a given scene with a scene transition
```csharp
public static void LoadScene(string sceneName)
```

### LoadSceneAsync(string sceneName, bool useLoadingWidget)
Loads a given scene with a scene transition, but loads it asynchronously with an optional loading widget.
```csharp
public static void LoadSceneAsync(string sceneName, bool useLoadingWidget = true)
```