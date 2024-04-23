# Shop
> namespace Gamekit2D.Runtime.Shops
```csharp
public class Shop : IInventory
```
## Summary
A shop - basically an [Inventory](../Items/Inventory.md) which also has money. Use the [ShopManager](./ShopManager.md) class to
create transactions between two shops to buy and sell items.

## Fields
| Name | Type | Description |
|------|------|-------------|
| money | int | The amount of money or cash in this store |

## Methods
### SetMoney(int value)
Sets the money or funds available in this shop instance
```csharp
public void SetMoney(int value)
```

### AddMoney(int value)
Adds money to the funds available in this shop instance
```csharp
public void AddMoney(int value)
```

### RemoveMoney(int value)
Removes money from the funds available in this shop instance
```csharp
public void RemoveMoney(int value)
```

### ContainsItem(ItemProfile item, int amount)
Returns true if the shop contains the given item. If amount is specified, then it only returns true
if the item exists in the shop with the quantity greater than or equivalent to the given amount.
```csharp
public bool ContainsItem(ItemProfile item)
```
```csharp
public bool ContainsItem(ItemProfile item, int amount)
```

### AddItem(ItemProfile item, int amount)
Adds the item with the given amount to the shop as a sellable item.
```csharp
public void AddItem(ItemProfile item)
```
```csharp
public void AddItem(ItemProfile item, int amount)
```

### RemoveItem(ItemProfile item, int amount)
Removes the given item, and the given quantity of that item from the shop.
```csharp
public void RemoveItem(ItemProfile item)
```
```csharp
public void RemoveItem(ItemProfile item, int amount)
```