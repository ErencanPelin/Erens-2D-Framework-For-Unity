# WeaponProfile
> namespace Gamekit2D.Runtime.Items.Profiles
```csharp
public abstract class WeaponProfile : ItemProfile
```

## Summary
A weapon item in the inventory. Allows this item to be used by the [Combat](../../Actor/Combat.md) component.
Has stats and fields related to dealing damage. 

Note this class is abstract, to define your own melee weapons or ranged weapons, look at the respective [MeleeWeaponProfile](./MeleeWeaponProfile.md) and [RangedWeaponProfile](./RangedWeaponProfile.md) classes.

## Fields
| Name | Type | Description                                                                      |
|------|------|----------------------------------------------------------------------------------|
| holdToAttack | bool | Applies to the respective field in the [Combat](../../Actor/Combat.md) component |
| attackDelay | float | Applies to the respective field in the [Combat](../../Actor/Combat.md) component |
| damageDealt | float | Damage this weapon does. Applies to the respective field in the [Combat](../../Actor/Combat.md) component|
| attackCooldown | float | Time in seconds to wait before being able to attack with this weapon again. Applies to the respective field in the [Combat](../../Actor/Combat.md) component |
| knockbackForce | float | Knockback force dealt by this weapon. Applies to the respective field in the [Combat](../../Actor/Combat.md) component |
| criticalHitChance | float | Chance as a decimal this weapon has to deal a critical hit |
| criticalHitDamagePercent | float | Amount of extra damage to deal as a decimal percentage, when a critical hit is landed with this weapon |