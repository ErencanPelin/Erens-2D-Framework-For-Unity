# InteractableObject
> namespace Gamekit2D.Runtime.Interactables
```csharp
public abstract class InteractableObject : MonoBehaviour
```

## Summary
Different from an [InteractiveObject](./InteractableObject.md). This class also provides an
OnTriggerEnter and Exit function for when the player is focusing and unfocussing from this interactable.

This allows the interactable to require the player to press a key to do the interaction, or show text on screen
when a player is focused on the interactable.

## Fields
| Name                 | Type | Description                                     |
|----------------------|------|-------------------------------------------------|
| onPlayerEnterTrigger | UnityEvent | Invoked when player enters the trigger collider |
| onPlayerExitTrigger  | UnityEvent | Invoked when player exits trigger collider      |
| onInteractStarted    | UnityEvent | Invoked when the interaction starts             |