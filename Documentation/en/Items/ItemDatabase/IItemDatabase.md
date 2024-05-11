# IItemDatabase
> namespace Gamekit2D.Runtime.Items.ItemDatabase
```csharp
public interface IItemDatabase
```

## Summary
Used to mock the item database in unit tests. Also provides base implementation for a database

## Methods
### GetItemFromID(string itemID)
Returns the requested item from the database using the item's GUID ID.
```csharp
public ItemProfile? GetItemFromID(string itemID)
```

### HasCache()
If the database has already built the cache from the database JSON file then it returns true.
Otherwise returns false.
````csharp
public bool HasCache();
````

### RebuildCache()
Regenerates the cache for the database. The first time the cache is built, it reads the data
from the Database JSON file. When cache exists, GetItemFromID requests the item from the cache instead
of the database file (it's faster).
```csharp
public void RebuildCache();
```