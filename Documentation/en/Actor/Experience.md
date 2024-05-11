# Experience
> namespace Gamekit2D.Runtime.Actor
```csharp
public class Experience : MonoBehaviour
```

## Summary

## Fields
| Name | Type | Description |
|------|------|-------------|
| Level | int | Current level of this actor |
| xp | int | Current amount of xp on this actor. Once it reaches the max xp, this actor levels up, increasing the Level. |
| OnLevelUp | UnityEvent | Invoked when the actor reaches the next level. Useful if you want to play some special effects or audio when the user levels up |

## Methods
### AddXp(int value)
Adds the given amount of xp to the actor. Automatically levels the actor up if required.
```csharp
public void AddXp(int value)
```

### ResetXp()
Resets the xp back to zero, and level progress. The level remains the same, but any xp gathered between levels is lost.
```csharp
public void ResetXp()
```