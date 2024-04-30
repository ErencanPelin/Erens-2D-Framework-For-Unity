# TimeStutter
> namespace Gamekit2D.Runtime.Effects.SceneEffects

```csharp
public class TimeStutter : MonoBehaviour, IEffect
```

## Summary
SceneEffect, temporarily freezes time for a very short period of time. Can be invoked as an event by other objects in the inspector

## Fields
| Name | Type | Description |
|------|------|-------------|
| originalDuration | float | The duration that the effect lasts in realtime seconds. |

## Methods
### Play()
Freezes the game for the duration set. Useful for hit stop effects.