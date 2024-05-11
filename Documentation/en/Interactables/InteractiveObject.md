# InteractiveObject
> namespace Gamekit2D.Runtime.Interactables

```csharp
public abstract class InteractiveObject : MonoBehaviour
```

## Summary
The base class that all interactive elements within a game inherit from

## Field
| Name | Type | Description |
|------|------|-------------|
| OnInteract | UnityEvent | This event is invoked when the interactable object is interacted with. Let's you customise certain interaction behaviours from the unity inspector |

## Methods
### OnTriggerEnter2D(Collider2D collider)
The standard trigger collider method as provided by Unity, all interactables must implement
this abstract method.
```csharp
protected abstract void OnTriggerEnter2D(Collider2D collider);
```