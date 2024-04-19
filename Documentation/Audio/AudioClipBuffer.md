# AudioClipBuffer
> namespace Gamekit2D.Runtime.Audio
```csharp
public sealed class AudioClipBuffer : MonoBehaviour
```

## Summary
A component that provides an easy way to vary the audio clip to play.

## Fields
| Name | Type | Description                                                                                       |
|------|------|---------------------------------------------------------------------------------------------------|
| Clips | AudioClip[] | The collection of potential AudioClips that might be played when the Play()<br/>method is invoked |

## Methods
### Play()
Play a random clip in the buffer. Can be called via a UnityEvent.
```csharp
public void Play()
```