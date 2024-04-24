# ItemProfile
> namespace Gamekit2D.Runtime.Items.Profiles
```csharp
public abstract class ItemProfile : ScriptableObject
```

## Summary
Defines a base ScriptableObject item for the Inventory system. Every other item inherits from this base class.

ItemProfiles are stores in the [Inventory](./../Inventory.md).

## Fields
| Name | Type | Description |
|------|------|-------------|
| itemID | string | Unique identifier of this item. Uses GUID version 4, stored as a string value. Useful to compare if two items match |
| itemSprite | Sprite | Icon image of this item |
| maxStackSize | int | Maximum number of this item that can fit in an ItemSlot in the Inventory |
| itemShopValue | int | Value of this item in in-game currency. Used in the Shop system |