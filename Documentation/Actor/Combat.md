# Combat
> namespace Gamekit2D.Runtime.Actor
```csharp
public class Combat : MonoBehaviour
```

## Summary
andles the combat mechanics for the actor including attacking & getting hit

## Fields
| Name                                            | Type                                 | Description |
|-------------------------------------------------|--------------------------------------|-------------|
| combatType | [CombatType](../Enums/CombatType.md) | Type of combat behaviour to use |
| gunTransform | Transform | The transform of the gun object attached to this object. Used to rotate the gun to face the attacking direction. Required if CombatType is Shooter |
| bulletParticles | ParticleSystem | ParticleSystem to use for bullets. Shooter combat is handled via particle collisions |
| attackType | [AttackType](../Enums/AttackType.md) | Type of input to detect in order to attack |
| attackDirection | [AttackDirection](../Enums/AttackDirection) | Determines how the direction to attack in, or the direction of the attack raycast when using melee combat is calculated |
| attackDelay | float | Time in seconds to wait before casting the attackRay when using melee combat. Change this value if the attack ray is cast out of sync with your attack animation |
| invert | bool | Invert the attack ray direction. Useful if your sprite is facing the wrong way! |
| target | Transform | Transform of the object to aim at and to attack |
| holdToAttack | bool | When true and using OnMouseClick AttackType, then player can hold the mouse button to attack. If True and using AI, the character constantly attackers. If false and using AI, the character attacks only when the player enters its attackRay |
| doesTakeDamage | bool | When true, this actor will register damage to the health component. False if otherwise |
| damageDealt | float | Damage to deal to another actor when we attack it. Only works if the object being attacked has doesTakeDamage set to True |
| attackCoolDown | float | Time in seconds to wait after attacking, before we can attack again |
| invulnerableCooldown | float | Time in seconds to wait after taking damage, before this actor can take damage again |
| knockbackForce| float | Knockback force to deal to any object this actor attacks |
| weaponProfile | [WeaponProfile](../Items/Profiles/WeaponProfile.md) | The weapon item to use to automatically set any of the fields on this component to the values set on the Weapon item |
| reloadTime | float | Time in seconds it takes to reload our gun after we run out of ammo |
| maxAmmo | int | Maximum number of bullets we can fire before needing to reload |
| onReload | UnityEvent | Invoked when this actor reloads their gun. Useful if you want to play an audio clip when reloading |
| currentAmmo | int | Ammo left |
| attackRaySettings | [AttackRaySettings](../Actor/AttackRaySettings.md) | Raycast settings to use when casting the attack ray. Any object this ray hits will be 'hit' by this combat component. Only works for melee attacking |
| onGetHit | UnityEvent | Invoked when this actor is hit by another combat component |
| onAttack | UnityEvent | Invoked when this combat component performs a successful attack |
| onCriticalHit | UnityEvent | Invoked when this combat component successfully delivers a critical hit on another combat component |
| animateInvulnerability | bool | When true, this combat component plays an 'invulnerability' animation. Only works if it is setup in the attached Animator component |
| criticalHitChance | float | Chance between 0 and 1 for this combat component to land a critical hit |
| criticalHitDamagePercent | float | Amount of extra damage to deal when landing a critical hit. For example, 0.5 = 50% extra damage |

## Methods
### Reset()
Sets the default values for this component. Override this function to implement your own default settings. It's recommended you still call `base.Reset()`.
```csharp
protected virtual void Reset()
```

### Init()
Called on Awake(). Does the initialisation for this component. Override this method if you want to have your own custom initialisation on your own Combat implementation. It's recommended
you still call `base.Init()` to ensure all references are set.
```csharp
protected virtual void Init()
```

### OnAttackKeyPress(InputAction.CallbackContext context)
Invoked when the Attack button is pressed
```csharp
public void OnAttackKeyPress(InputAction.CallbackContext context)
```

### OnReloadKeyPress(InputAction.CallbackContext context)
Invoked when the Reload button is pressed, when the CombatType is set to Shooter
```csharp
public void OnReloadKeyPress(InputAction.CallbackContext context)
```

### BeInvulnerable()
Sets this GameObject to be 'Invulnerable' to combat for the default invulnerability time. 
```csharp
public void BeInvulnerable()
```

### SetAimAtTarget(Transform target)
Sets the target for this actor to aim at, **Does not** change the attack or aim SpriteDirection. Can also be invoked
as a UnityEvent from inside the inspector window.
```csharp
public void SetAimAtTarget(Transform target)
```