# Teleporter
> namespace Gamekit2D.Runtime.Interactables
```csharp
public sealed class Teleporter : InteractiveObject
```
## Summary
Teleporters act as portals. When the player enters this teleporter's Trigger collider, their position is set to the location set
to the PartnerLocation teleporter.

## Fields
| Name | Type | Description |
|------|------|-------------|
| partnerLocation | [Teleporter](./Teleporter.md) | The exit location of this teleporter |
| onTeleportAway | UnityEvent | Invoked when the player enters this teleporter and is teleported to the partner location |
| onTeleportTo | UnityEvent | Invoked when the player has teleported to this teleporter, from another teleporter |