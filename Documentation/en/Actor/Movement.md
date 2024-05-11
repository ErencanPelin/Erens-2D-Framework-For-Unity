# Movement
> namespace Gamekit2D.Runtime.Actor

```csharp
public class Movement : MonoBehaviour
```

## Summary
The actor class which handles all movement controls for a 2D character. Requires the Actor class, Rigidbody2D and a CapsuleCollider2D
attached to a gameObject to work properly

## Fields
| Name | Type | Description                                                                                                                                                                                             |
|------|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| actorType | [ActorType](./../Enums/ActorType.md) | The type of movement behaviour to use                                                                                                                                                                   |
| gravityForce | float | Force of gravity to apply                                                                                                                                                                               |
| maxFallSpeed | float | Maximum velocity this actor can fall at                                                                                                                                                                 |
| maxJumpVelocity | float | Maximum velocity this actor can jump. Also the maximum velocity the player can move on the Y-Axis                                                                                                       |
| jumpForce | float | Force of velocity to apply when the actor jumps                                                                                                                                                         |
| airControlPercent | float | Decimal percent between 0f and 1f. Defines how much control the actor has of it's movement while in the air. 0.5 = half as much control, 1f = full(normal) control                                      |
| doubleJumpMinThreshold | float | The minimum required velocity for this actor to have before they can double jump                                                                                                                        |
| doubleJumpMaxThreshold | float | The maximum required velocity for this actor to have before they can double jump. Pair this with doubleJumpMinVelocity to create a threshold for when the actor is in the air that they can double jump |
| canDoubleJump | bool | When true, allows this actor to jump ONCE while they are in the air                                                                                                                                     |
| inputType | [InputType](./../Enums/InputType.md) | Type of input used to control this actor's movement behaviour                                                                                                                                           |
| target | Transform | The transform target for this actor to follow if InputType is set to Target                                                                                                                             |
| moveSpeed | float | The speed at which this actor moves at                                                                                                                                                                  |
| moveSmoothing | float | The amount of smoothing to apply to this actor's movement. Allows you to control how 'slidey' the character is                                                                                          |
| canDash | bool | When true, the player can Dash when they press the 'Dash' key                                                                                                                                           |
| dashForce | float | The speed or force the character dashes at                                                                                                                                                              |
| dashCooldown | float | Time in seconds the player must wait between dashing                                                                                                                                                    |
| followAIRange | float | Range the player must be in before this movement component detects them and follows them. Used when InputType is set to FollowAI                                                                        |
| pathReference | [Path](./../Paths/Path.md) | The path for this movement component to follow when InputType is set to Path                                                                                                                            |
| onJump | UnityEvent | Invoked whenever this actor jumps. Useful for spawning effects like jump particles                                                                                                                      |
| onDash | UnityEvent | Invoked whenver the player dashes. Useful for dash animations, sound effects or visual effects                                                                                                          |
| onDoubleJump | UnityEvent | Invoked whenever the actor double jumps in mid air. Useful for visual, sound or animation effects                                                                                                       |
| groundCheckSettings | [RaySettings](./RaySettings.md) | The raycast settings used to control how the ground check raycast behaves                                                                                                                               |
| _transform | Transform | The transform reference to the Transform attached to this movement component. A cached, optimised reference                                                                                             |
| rb | Rigidbody2D | The rigidbody2D component attached to this Movement component                                                                                                                                           |
| velocity | Vector2 | Protected. Holds the current velocity of this movement component                                                                                                                                        |
| Velocity | Vector2 | Public version to this movement component's current velocity |
| onGround | bool | Result of the ground check |

## Methods
### Init()
Initialisation - sets the rigidbody and transform references - can be overridden
```csharp
protected virtual void Init()
```

### CalculateMovement()
Calculates the velocity to move in and returns the velocity - can be overridden
```csharp
protected Vector2 CalculateMovement()
```

### SetFollowTarget(Transform target)
Sets the follow for this actor to follow, also sets the input type to InputType.Target if it is not already set. Can also be invoked
as a UnityEvent from inside the inspector window.
```csharp
public void SetFollowTarget(Transform target)
```

### Knockback(Vector2 direction, float force)
Applies a short burst force in the given direction.
```csharp
public void Knockback(Vector2 direction, float force)
```