# PowerSupplyObject
> namespace Gamekit2D.Runtime.Interactables.Power
```csharp
public abstract class PowerSupplyObject : ActionInteractiveObject
```

## Summary
Provides power to a [PoweredObject](./PoweredObject.md) object

## Fields
| Name | Type | Description |
|------|------|-------------|
| isOn | bool | Whether this power supply is producing power or not |
| onSprite | Sprite | Sprite texture to display when this power supply object is On |
| offSprite | Sprite | Sprite texture to display when this power supply object is off |
| listeners | List<[PoweredObject](./PoweredObject.md)> | The group of target powered objects that will be switched on and off with this power supply |

## Methods
### OnActivate
Triggered when a player interacts with this object. Should control how power behaves on this PowerSupply object
```csharp
protected abstract void OnActivate();
```