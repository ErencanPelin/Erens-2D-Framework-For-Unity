# SpriteDirection
> namespace Gamekit2D.Runtime.Actor

```csharp
public class SpriteDirection : MonoBehaviour
```

## Summary
Handles the direction for the sprite to face

## Fields
| Name | Type                                         | Description |
|------|----------------------------------------------|-------------|
| invertDirection | bool                                         | When true, the sprite faces the opposite way than what this class outputs |
| faceDirection | [DirectionType](./../Enums/DirectionType.md) | How the sprite's direction is calculated |
| lookAtTarget | Transform                                    | The target used for calculating the sprite facing direction if the DirectionType is set to target |

## Methods
### Init()
Initialises the Component - can be overridden, - called on Awake()
```csharp
protected virtual void Init()
```

### CalculateDirection()
Calculate the desired scale for this actor and return it as a type.
```csharp
protected virtual Vector2 CalculateDirection()
```

### SetLookAtTarget(Transform target)
Sets the target for this actor to look at, also sets the SpriteDirection type to DirectionType.Target if it is not already set. Can also be invoked
as a UnityEvent from inside the inspector window.
```csharp
public void SetLookAtTarget(Transform target)
```