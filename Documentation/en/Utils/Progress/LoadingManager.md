# Loading Manager
> namespace Gamekit2D.Runtime.Utils.Progress
```csharp
public sealed class LoadingManager : Singleton<LoadingManager>
```

## Summary
Attached to the Systems prefab, Handles displaying the loading bar (if any)
when loading a new scene or performing an async behaviour (like saving)

## Methods
### Show(int min, int max)
Show the loading bar with the given start and end values
```csharp
public static void Show(int min, int max)
```

### Report(int value)
Updates the current loading bar with the given value
```csharp
public static void Report(int value) => progress.Report(value);
```

### Hide()
Stops showing the current loading bar
```csharp
public static void Hide()
```