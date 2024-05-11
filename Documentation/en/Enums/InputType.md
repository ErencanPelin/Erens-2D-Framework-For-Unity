# InputType
> namespace Gamekit2D.Runtime.Enums

```csharp
public enum InputType
{
    keyboard, //move with keyboard or gamepad input (any user input)
    follow, //Always follow a given target
    mouseClick, //move to the mouse position when the mouse clicks somewhere
    mouseFollow, //always move toward the mouse cursor
    followAI, //Follow a given target when that target enters a given range
    path //Follow a set path
}
```

## Summary
Type of input used to move the player or actor. Used on the [Movement](../Actor/Movement.md) component.
