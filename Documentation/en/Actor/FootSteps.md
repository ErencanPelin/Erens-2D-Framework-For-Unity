# FootSteps
> namespace Gamekit2D.Runtime.Actor
```csharp
public sealed class FootSteps : MonoBehaviour
```

## Summary
Handles playing foot step sound effects using the distance the actor travels.

## Fields
| Name | Type | Description |
|------|------|-------------|
| onStep | UnityEvent | Invoked each time the player 'steps'. Use this event to setup sound or visual effects to run each time the player steps |
| interval | float | Distance required to travel between steps. Play around with this value to get it sounding right for your player and animation |
