# CameraShake
> namespace Gamekit2D.Runtime.Effects.SceneEffects

```csharp
public class CameraShake : MonoBehaviour, IEffect
```

## Summary
Attach to the Camera GameObject, the Perform method can be called to do the shake behaviour

## Fields
| Name | Type | Duration |
|------|------|----------|
| shakeDuration | float | The length of time the effect lasts for in realtime seconds |
| strength | float | How strong the shaking effect should be |

## Methods
### Play()
Plays the camera shake effect. Useful for 'impact' such as when the player gets hit.