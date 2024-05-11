# Checkpoint
> namespace Gamekit2D.Runtime.Interactables
```csharp
public sealed class Checkpoint : InteractiveObject
```

## Summary
A checkpoint acts as a respawn point. It simply sets the respawn location for the [CheckpointListener](./../Actor/CheckpointListener.md) component attached to the Player.
When the player enters this checkpoint's trigger, their respawn position is set.