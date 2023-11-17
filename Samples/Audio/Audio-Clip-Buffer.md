# Audio Clip Buffer
> Gamekit2D.Runtime.Audio / Inherits from MonoBehaviour / Sealed / Requires AudioSource
<br>

This component stores an array of AudioClips that can be set via the inspector window, and played from both within code, and as a UnityEvent.

```cs
using Gamekit2D.Runtime.Audio;

public class ExampleClass : MonoBehaviour
{
  [SerializeField] private AudioClipBuffer audioClipBuffer;

  private void Awake()
  {
    audioClipBuffer = GetComponent<AudioClipBuffer>();
    audioClipBuffer.Play();
  }
}
```

## Public Methods
- [Play](#audioclipbuffer.play)

---

## AudioClipBuffer.Play
### Description
Plays a random clip from the array of saved clips. Can also be invoked as a UnityEvent from the Unity inspector window.
