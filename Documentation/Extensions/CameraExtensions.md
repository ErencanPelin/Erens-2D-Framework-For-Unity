# CameraExtensions
> namespace Gamekit2D.Runtime.Extensions
```csharp
public static class CameraExtensions
```

## Summary
Extension methods for Camera class

## Methods
### GetInGameCursorPosition(this PlayerInput playerInput)
Retrieves the position of the cursor in game coordinates. If the input source is a Gamepad, then it calculates the cursor position
via the look direction of the left stick
```csharp
public static Vector2 GetInGameCursorPosition(this PlayerInput playerInput)
```