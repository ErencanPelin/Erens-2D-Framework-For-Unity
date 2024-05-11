# Checkpoint Listener
> namespace Gamekit2D.Runtime.Actor
```csharp
public class CheckpointListener : MonoBehaviour
```

## Summary
Allows this actor to trigger checkpoints and save their spawn position

## Fields
| Name | Type | Description |
|------|------|-------------|
| onResetKeyPressed | UnityEvent | Event is invoked whenver the player manually presses the key bound to 'reset' the level or player. Useful in certain puzzle platformers. |

## Methods
### Init()
Initialises the component, - can be overriden, called in Awake()
```csharp
protected virtual void Init()
```

### SetSpawn(Vector2 position)
Sets the respawn position of this actor to a given position
```csharp
public void SetSpawn(Vector2 position)
```

### GoToLastCheckpoint()
Teleports the actor to their last saved spawnPoint position
```csharp
public void GoToLastCheckpoint()
```