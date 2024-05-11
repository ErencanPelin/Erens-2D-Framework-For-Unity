# PoweredObject
> namespace Gamekit2D.Runtime.Interactables.Power
```csharp
public sealed class PoweredObject : MonoBehaviour
```

## Summary
Is an object that can be powered via a [PowerSupplyObject](./PowerSupplyObject.md).

## Fields
| Name | Type | Description |
|------|------|-------------|
| logicGate | [Gate](./../../Enums/Gate.md) | The type of logic gate to use when setting the IsOn state of this powered object |
| onPowerOn | UnityEvent | Invoked when the powered state of this object becomes true |
| onPowerOff | UnityEvent | Invoked when the powered state of this object becomes false |
       
## Methods
### AddListener([PowerSupplyObject](./PowerSupplyObject.md))
Adds a power source this object will listen to when updating its on/off state.
```csharp
public void AddListener(PowerSupplyObject PS)
```

### RemoveListener([PowerSupplyObject](./PowerSupplyObject.md))
Removes a power source from the list of sources this object will listen to when updating its on/off state.
```csharp
public void RemoveListener(PowerSupplyObject PS)
```

### UpdatePower()
Updates the on/off state of this object based on the on/off state of it's listening sources.
```csharp
public void UpdatePower()
```