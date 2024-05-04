# IInventory
> namespace Gamekit2D.Runtime.Items

```csharp
public interface IInventory
```

## Summary
Provides generic inventory functions

## Methods
### AddItem
Used to add an item into an inventory
```csharp
public void AddItem(ItemProfile item);
```
```csharp
public void AddItem(ItemProfile item, int amount);
```

### RemoveItem
Used to remove an item from an inventory
```csharp
public void RemoveItem(ItemProfile item);
```
```csharp
public void RemoveItem(ItemProfile item, int amount);
```

### Contains
Used to return true if the inventory contains a given item
```csharp
public bool ContainsItem(ItemProfile item);
```
```csharp
public bool ContainsItem(ItemProfile item, int amount);
```