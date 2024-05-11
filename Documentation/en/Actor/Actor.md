# Actor
> namespace Gamekit2D.Runtime.Actor
```csharp
public class Actor : MonoBehaviour
```

## Summary
The main Actor component which all other components rely on.

## Methods
### Reset()
Sets default values of this actor. Can be overridden by a child class if you wanted to define custom default values for this component.
```csharp
protected virtual void Reset()
```

### Destroy(float seconds)
Simply destroys this actor gameObject and removes it from the scene after the given amount of seconds has passed.

Exposing this function allows you to destroy a GameObject via a Unity Event in the Inspector.
```csharp
public void Destroy(float seconds)
```
