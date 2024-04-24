# SaveProfileData
> namespace Gamekit2D.Runtime.Utils.SaveLoad
```csharp
public abstract record SaveProfileData
```

## Summary
Defines a save profile that is saved via the [SaveManager](./SaveManager.md). Save profiles can be loaded via the
[SaveManager](./SaveManager.md) as well. Create your own SaveProfileData by inheriting this class to define custom data
that your game should save.

The save system uses json serialization, and so almost any c# object can be saved, including arrays, lists and collections.

## Methods
### SaveAsAsync(string saveName, bool overwrite, bool encrypt)
Saves all data in this save profile asynchronously. Useful for automsaves. Optional settings for encrypting the save file or keeping it plain JSON.

It is recommended you encrypt all saves in a production build, but for debugging and testing, leaving encryption off maybe useful.

By default, trying to save a profile with the same name as an existing save profile will throw and error. Change `overwrite` to `true` if you would like to
instead permanently delete any data in that existing save profile, and write new data over it.
```csharp
public async void SaveAsAsync(string saveName, bool overwrite = false, bool encrypt = true)
```

### SaveAs(string saveName, bool overwrite, bool encrypt)
Same as [SaveAsAsync](#saveasasyncstring-savename-bool-overwrite-bool-encrypt), but without asynchronous tasks. Easier to use, but might affect
performance during saving processes.
```csharp
public void SaveAs(string saveName, bool overwrite = false, bool encrypt = true)
```