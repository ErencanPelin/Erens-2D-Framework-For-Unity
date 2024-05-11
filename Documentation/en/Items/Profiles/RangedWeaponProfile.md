# RangedWeaponProfile
> namespace Gamekit2D.Runtime.Items.Profiles
```csharp
public class RangedWeaponProfile : WeaponProfile
```

## Summary
Builds onto the [WeaponProfile](./WeaponProfile.md) class by adding specific settings that apply to ranged weapons such as guns, bows, magic, etc.

## Fields
| Name | Type | Description |
|------|------|-------------|
| gunSprite | Sprite | Sprite to use for the gun's graphic in the game. This does not apply to the bullets, just the gun graphic shown on the player. |
| reloadTime | float | Time in seconds it takes for this weapon to reload after running out of ammo |
| maxAmmo | int | Starting ammo for this gun, or the number of bullets that can be fired before needing to reload |