# Health
> namespace Gamekit2D.Runtime.Actor
```csharp
public class Health : MonoBehaviour
```

## Summary
Controls health behaviour for this actor, including taking damage or displaying health value
onto a health bar GUI. This class also controls what to do when this actor dies.

## Fields
| Name | Type | Description |
|------|------|-------------|
| maxHealth | float | The maximum amount of health points this actor can have. Also the starting health value for this actor |
| doNaturalRegeneration | bool | When true, this actor can slowly regenerate lost health over time |
| naturalRegenAmount | float | The amount of health points to add over time when doNaturalRegeneration is set to True |
| curHealth | float | The current health of this actor |
| healthSlider | Slider | The GUI slider to display this health component onto |
| onDeath | UnityEvent | Invoked when this actor's curHealth == 0 |

## Methods
### Init()
Initialises the component. Can be overridden for custom init behaviour.
```csharp
protected virtual void Init()
```

### NegateHealth(float amount)
Negates a given value from the actor's health. If health is then 0, the function invokes the 'OnDeath' event
```csharp
public void NegateHealth(float amount)
```

### AddHeath(float amount)
Adds a given value to the actor's health.
```csharp
public void AddHealth(float amount)
```

### SetHealth(float value)
Sets the value of the Actor's current health
```csharp
public void SetHealth(float value)
```