# ServiceLocator
> namespace Gamekit2D.Runtime.Services
```csharp
public static class ServiceLocator
```

## Summary
Static classes allows you to find a class tagged with the IService interface. In most use cases using the Game kit, you will not need to use this class. This should only be used by or changed and
modified by advanced C# users.

## Methods
### Resolve<T>()
Finds and returns the class with the given type. For example, if `MyClass` inherits from `IService`, I can `Resolve<MyClass>()`
```csharp
public static T Resolve<T>() where T : IService
```