# Loading Widget
> namespace Gamekit2D.Runtime.Utils.Progress
```csharp
public abstract class LoadingWidget : MonoBehaviour
```

## Summary
A widget (GameObject) which does something to indicate some progression or loading value.
Implement this class to create custom loading bar or progress indicator behaviours

## Methods
### Show(int min, int max)
Shows the loading widget by setting the start and end values of the loading progress indicator
```csharp
public abstract void Show(int min, int max);
```

### UpdateProgress(int currentProgress)
Report progress to this loading widget, sets the current progress to the new given value
```csharp
public abstract void UpdateProgress(int currentProgress);
```