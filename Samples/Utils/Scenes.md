# Scenes
> Gamekit2D.Runtime.Utils / Inherits from Singleton / Sealed
<br>

This class is designed to override the existing UnityEngine.SceneManagement functionality. It builds onto SceneManagement by automatically handling scene transitions.

Note, Scenes class does NOT currently support loading scenes with scene assets or scene indexes.

```cs
using Gamekit2D.Runtime.Utils;

public class ExampleClass : MonoBehaviour
{
  private void Start()
  {
    Scenes.LoadScene("Next_Scene");
  }
}
```

## Public Methods
- [LoadScene](#loadscene)
- [LoadSceneAsync](#loadsceneasync)

---

## LoadScene
```cs
Scenes.LoadScene("StartScene");
```
### Description
Load a scene the same way as SceneManagement.
### Parameters
| Name | Type | Description |
|-|-|-|
| sceneName | string | Name of scene to be loaded. |

---

## LoadSceneAsync
```cs
Scenes.LoadSceneAsync("StartScene", useLoadingWidget: false);
```
### Description
Loads a given scene asynchronously.
### Parameters
| Name | Type | Description |
|-|-|-|
| sceneName | string | Name of scene to be loaded. |
| useLoadingWidget | bool | When true, the globally selected loading widget will be shown while the scene is loading in the background. Default is true. |
