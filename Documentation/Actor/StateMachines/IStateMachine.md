# IStateMachine
> namespace Gamekit2D.Runtime.Actor.StateMachines

## Summary
The base StateMachine interface, implemented by a [StateMachine](StateMachine.md)

## Methods
### ChangeState([IState](IState.md) newState)
Used to change the current state of this StateMachine.
```cs
public void ChangeState(IState newState);
```

## Example
```cs
public class StateMachine : MonoBehaviour, IStateMachine
{
    private IState startingState;
    private IState currentState;

    private void Start()
    {
        ChangeState(startingState);
    }

    // every frame we update the current state
    private void Update() =>  currentState.Update();

    // every physics frame we update the physics of the state.
    // useful for if this state controls Rigidbody2D movement
    private void FixedUpdate() => currentState.PhysicsUpdate();

    // Changes the current state into the new State
    public void ChangeState(IState newState)
    {
        if (newState == currentState) return;
        currentState?.Exit();
        currentState = newState;
        currentState.Enter();
    }
}
```