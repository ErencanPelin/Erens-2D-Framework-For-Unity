# Path
> namespace Gamekit2D.Runtime.Paths

```csharp
public class Path : MonoBehaviour
```

## Summary
A path or list of points to define a track. 

Other components such as [MovingPlatform](../LevelTiles/MovingPlatform.md) use this to define their movement path.

## Fields
| Name | Type                             | Description                                                                       |
|------|----------------------------------|-----------------------------------------------------------------------------------|
| pathType | [PathType](../Enums/PathType.md) | The type of this path, see [PathType](../Enums/PathType.md) for full description. |
| points | List\<Vector2\>                  | The points along this path. Modify this to change the shape of the path |