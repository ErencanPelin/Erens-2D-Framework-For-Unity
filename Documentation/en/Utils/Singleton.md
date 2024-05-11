# Singleton
> namespace Gamekit2D.Runtime.Utils

```csharp
public class Singleton<T> : MonoBehaviour where T : Singleton<T>
```

## Summary
Provides a generic singleton implementation.

## Properties
### Instance
Returns the current instance of this singleton.
```csharp
public static T Instance
```