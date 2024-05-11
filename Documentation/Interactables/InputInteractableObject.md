# InputInteractableObject
> namespace Gamekit2D.Runtime.Interactables
```csharp
public class InputInteractableObject : InteractableObject
```

## Summary
Builds onto the [InteractableObject](./InteractableObject.md) class. This class enabled the ability to require the player to press the set 'interact' key or input in order to interact with the object.

## Fields
| Name | Type | Description |
|------|------|-------------|
| interactKeyHintText | TMP_Text | The reference to the on-screen Text GUI to display the key to press in order to interact with this object |
| interactHintPrefixText | string | The string text to display before the key. E.g. `Press E` |
| interacttHintColor | Color | Color of the key displayed in the hint text |