# Animation
> namespace Gamekit2D.Runtime.Actor
```csharp
public class Animation : MonoBehaviour
```

## Summary
Handles any animation for an [Actor](Actor.md).

## Methods
### Init()
Is called on Awake(). Does any initialisation for this component. 

You can Override this component in any child class to provide custom Animation behaviour.
```csharp
protected virtual void Init()
```

### UpdateAnimations()
Updates all animation values on the attached animator. Can be overridden, however you should call `base.UpdateAnimations();`
```csharp
protected virtual void UpdateAnimations()
```

### SetTrigger(string triggerName)
Enables a trigger parameter on the animator, can also be invoked as a UnityEvent from the Inspector
```csharp
public void SetTrigger(string triggerName)
```

### SetBool(string name, bool value)
Sets a given bool parameter on the animator to a given value
```csharp
public void SetBool(string name, bool value)
```

### SetInt(string name, int value)
Sets a given int parameter on the animator to a given value
```csharp
public void SetInt(string name, int value)
```

### SetFloat(string name, float value)
Sets a given float parameter on the animator to a given value
```csharp
public void SetInt(string name, float value)
```

### ToggleBool(string name)
Toggles the value of a given bool parameter on the animator. If it was true, it becomes false, and if it was false, it becomes true

This function can be invoked via a UnityEvent in the Inspector.
```csharp
public void ToggleBool(string name)
```