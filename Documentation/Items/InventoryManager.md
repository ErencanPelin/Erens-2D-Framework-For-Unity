# InventoryManager
> namespace Gamekit2D.Runtime.Items
```csharp
public static class InventoryManager
```

## Summary
Handles interactions between different IInventory objects

## Methods
### MoveItem
Moves the given item from one inventory to another
```csharp
public static bool MoveItem(IInventory inventoryA, IInventory inventoryB, ItemProfile item, int amount = 1)
```
