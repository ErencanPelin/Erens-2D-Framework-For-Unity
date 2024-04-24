# Saves
> namespace Gamekit2D.Runtime.Utils.SaveLoad
```csharp
public static class Saves
```

## Summary
This class provides some default setups for SaveProfiles. Namely, a default profile for inventory saving and a default profile for player save data.
Feel free to use these records for save profiles, alternatively it's recommended to inherit your own class from [SaveProfileData](./SaveProfile.md)
and define your own save data.

## Records
```csharp
public record InventorySaveData : SaveProfileData
{
    public Inventory inventoryData;
}
```
```csharp
public record PlayerSaveData : SaveProfileData
{
    public Vector3 position;
    public int currentLevel;
    public float health;
    public float xp;
}
```