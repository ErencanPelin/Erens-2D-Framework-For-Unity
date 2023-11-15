# Scenes
This class is designed to override the existing UnityEngine.SceneManagement functionality. It builds onto SceneManagement by automatically handling scene transitions.

Note, Scenes class does NOT currently support loading scenes with scene assets or scene indexes.

## Contents
- LoadScene
- LoadSceneAsync

---

# LoadScene
Load a scene the same way as SceneManagement with the following line:
```cs
using Gamekit2D.Runtime.Utils;

Scenes.LoadScene(string sceneName);
```
For example:
```cs
Scenes.LoadScene("StartScene");
```

# LoadSceneAsync
Loads a given scene asynchronously:
```cs
Scenes.LoadSceneAsync("StartScene");
```
