# Inventory
> namespace Gamekit2D.Runtime.Items
```csharp
public sealed class Inventory : IInventory
```

## Summary
Implements the [IInventory](./IInventory.md) interface. Defines an inventory that contains items.
Items in the inventory are stored as an [InventoryItemData](./InventoryItemData.md) object.
This class handles all backend for an inventory. Use [InventoryObject](./InventoryObject.md) to attach an Inventory
to a Monobehaviour.

## Constructor
Creates a new blank inventory with a max of 0. <b>Should only be used by the Unity Inspector.</b>
If you are creating the inventory through code, please provide a size.
```csharp
public Inventory()
```
Initialises a new inventory instance with the given parameters. The size parameter
dictates how many 'slots' this inventory should have. Each slot can fit up to the max stack size of each
item as defined in their [ItemProfile](./Profiles/ItemProfile.md).
**It's recommended you leave the itemDatabase parameter null except in exceptional circumstances**.
```csharp
public Inventory(int size, IItemDatabase itemDatabase = null)
```

## Methods
### AddItem
Adds the the given quantity amount of the given item to the inventory. If no quantity is provided, automatically defaults to 1. The item is added to the next empty slot if there is space. Stacks automatically. Item is deleted if the inventory is full.
```csharp
public void AddItem(ItemProfile item, int quantity)
```
```csharp
public void AddItem(ItemProfile item)
```        

### RemoveItem
Removes the given quantity of the given item from the inventory. Removes it from a stack if one exists. Nothing happens if the item doesn't exist in the inventory. If no quantity
is provided, the quantity automatically defaults to 1.
```csharp
public void RemoveItem(ItemProfile item, int quantity)
```
```csharp
public void RemoveItem(ItemProfile item)
```

### GetItemAt(int index)
Returns the itemData at the given index. Throws an error if the index is out of bounds.
```csharp
public InventoryItemData GetItemAt(int index)
```

### ContainsItem
Returns true if a given item exists in the inventory, AND there is at least the given quantity amount in the inventory.
If no quantity is provided, the the quantity automatically defaults to 1.
```csharp
public bool ContainsItem(ItemProfile item, int quantity)
```
```csharp
public bool ContainsItem(ItemProfile item) => Contains(item, 1);
```

### ClearAllItems()
Permanently deletes every item in the inventory. This is irreversible. All data will be lost!
```csharp
public void ClearAllItems() => items = new InventoryItemData[size];
```

### RemoveAllItemsOfType(ItemProfile item)
Removes every item in the inventory of the given type
```csharp
public void RemoveAllItemsOfType(ItemProfile item)
```