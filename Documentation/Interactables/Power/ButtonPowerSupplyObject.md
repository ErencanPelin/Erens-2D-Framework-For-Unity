## Button Power Supply Object
> namespace Gamekit2D.Runtime.Interactables.Power
```csharp
public sealed class ButtonPowerSupplyObject : PowerSupplyObject
```

## Summary
Implements the [PowerSupplyObject](./PowerSupplyObject.md). Acts as a button that has customisable behaviour.

When ButtonType is `weighted', this button is active so long as there is at least one player standing on the button.
If there are no players on the button, then it turns off.

Alternatively, if the ButtonType is 'timed', this button automatically turns itself off after the set amount of time - regardless if there
are players standing on the button or not.

## Fields
| Name | Type | Description |
|------|------|-------------|
| activeTime | float | The time in seconds this button stays on for if the ButtonType is set to `timed` |
| buttonType | ButtonType | The type of button this button is. Controls button behaviour |