# IState
> namespace Gamekit2D.Runtime.Actor.StateMachines

## Summary
The base state interface used by a [StateMachine](StateMachine.md). Implemented by a [State](State.md).

## Methods
### Enter()
Called when a StateMachine transitions to this State.
```cs
public void Enter();
 ```

### Update()
Called every Update() frame while this state is active.
```csharp
public void Update();
```

### Physics Update()
Called every FixedUpdate() frame while this state is active.
```csharp
public void PhysicsUpdate();
```

### Exit
Called at the end of this State, or when we switch away from it.
```csharp
public void Exit();
```
