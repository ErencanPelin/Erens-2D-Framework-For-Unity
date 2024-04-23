# ShopManage
> namespace Gamekit2D.Runtime.Shops
```csharp
public static class ShopManager
```

## Summary
Handles transactions between shops

## Delegates
### TransactionFailedCallback()
Invoked if a requested transaction was failed. Either due to missing items, or missing funds.
```csharp
public delegate void TransactionFailedCallback();
```
### TransactionSuccessCallback()
Invoked when a transaction was successfully completed
```csharp
public delegate void TransactionSuccessCallback();
```

## Methods
### CreateTransaction(...)
Creates a new transaction between two shops to trade items, and the respective value (money) for the items.
Returns True if the transaction was successful, false if otherwise.
Create your own action from the delegates above to utilise in methods below.
```csharp
public static bool CreateTransaction(Shop buyer, Shop seller, ItemProfile item, int amount, TransactionFailedCallback errorCallback = null, TransactionSuccessCallback successCallback = null)
```
```csharp
public static bool CreateTransaction(Shop buyer, Shop seller, ItemProfile item, TransactionFailedCallback errorCallback = null, TransactionSuccessCallback successCallback = null)
```