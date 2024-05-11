# InventoryItemData
> namespace Gamekit2D.Runtime.Items
```csharp
public struct InventoryItemData
```

## Summary
Contains an item reference. Used in the [Inventory](./Inventory.md). Item's are stored in the inventory
as IDs only, this makes it easier to compare items in the code. There is a custom editor that makes it simple
to add item profiles to an inventory via the Unity inspector, but all items are stored as IDs and then 
the ItemDatabase helps turn IDs into [ItemProfiles](./Profiles/ItemProfile.md).

Another benefit of using IDs is the ability to serialize and deserialize them easier for the Saving and loading 
system so that the inventory can be saved just via the item id instead of the entire item profile.

## Constructors
Creates a new instance of this struct using the given parameters.
```csharp
public InventoryItemData(string itemID, int quantity)
```

## Fields
| Name | Type | Description |
|------|------|-------------|
| itemID | string | Stringified unique GUID of the [ItemProfile](./Profiles/ItemProfile.md) stored in this inventory slot |
| quantity | int | Number of items in this slot |