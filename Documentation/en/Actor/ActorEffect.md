# Actor
> namespace Gamekit2D.Runtime.Actor
```csharp
public class ActorEffect : MonoBehaviour
```

## Summary
Handles all effects on actors or objects within a scene which create/emit effects

## Fields
| Name     | Type  | Description                                                                                                        |
|----------|-------|--------------------------------------------------------------------------------------------------------------------|
| isGlobal | bool  | When true, this effect exists beyond the lifeTime of this GameObject and is not a child of this object's Transform |
| lifeTime | float | Number is Seconds, this Effect lives for. Effect object is automatically destroyed after. |

## Methods
### Play(ParticleSystem particles)
Spawns a particle system and then destroys it after the set lifeTime. Can also be invoked from the inspector as a UnityEvent.
```csharp
public void Play(ParticleSystem particles)
```