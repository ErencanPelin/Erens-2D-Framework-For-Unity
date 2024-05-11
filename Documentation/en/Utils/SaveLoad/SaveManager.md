# SaveManager
> namespace Gamekit2D.Runtime.Utils.SaveLoad
```csharp
public static class SaveManager
```

## Summary
Handles all loading functionality. This save system uses Newtonsoft Json to save & load encrypted JSON files of data.

## Methods
### DeleteSaveAsync(string profileName)
Deletes a given save from the saves folder. This method is asynchronous, and the game will continue playing as the file is being deleted in the background
```csharp
public static async Task DeleteSaveAsync(string profileName)
```

### DeleteSave(string profileName
Deletes a given save from the saves folder. This method is NOT asynchronous, and may halt the main game loop while the file is being deleted.
```csharp
public static void DeleteSave(string profileName)
```

### LoadAsAsync\<T>(string profileName, bool encryptionEnabled)
Loads and returns a [SaveProfile](./SaveProfile.md) from the Saves Folder. Uses the given profile name to retrieve the file.
The file is automatically decrypted and turned into a [SaveProfile](./SaveProfile.md) object of the given type. This method is asynchronous and should be awaited for its Result.
```csharp
public static async Task<SaveProfile<T>> LoadAsAsync<T>(string profileName, bool encryptionEnabled = true) where T : SaveProfileData
```

### LoadAs\<T>(string profileName, bool encryptionEnabled)
Loads and returns a SaveProfile from the Saves Folder. Uses the given profile name to retrieve the file.
The file is automatically decrypted and turned into a SaveProfile object of the given type. This method is asynchronous and should be awaited for its Result.
```csharp
public static SaveProfile<T> LoadAs<T>(string profileName, bool encryptionEnabled = true) where T : SaveProfileData
```