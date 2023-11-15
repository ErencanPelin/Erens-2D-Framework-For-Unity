# Save Load System
## Contents:
- [Save Data Objects](#save-data-objects)
- [Saving SaveData Objects](#saving-savedata-objects)
- [Loading SaveData OBjects](#loading-savedata-objects)
- [Delete Saves](#deleting-saves)

---

# Save Data Overview
The save load system works by serializing [SaveData](#custom-save-data) objects into JSON format, and then writing the JSON string into a text file inside the ["Application.PersistentDataPath"](https://docs.unity3d.com/ScriptReference/Application-persistentDataPath.html) 
directory.

By default, the save load system contains 2 SaveData preset objects:
1. [PlayerSaveData](#playersavedata)
2. [InventorySaveData](#inventorysavedata)

However, it is possible to define your own [Custom Save Data](#custom-save-data) Object to store any data you find necessary.

---

# Save Data Objects
## PlayerSaveData
This is a preset class designed to make it easier to save common values that a player might have.

To create your own playerSaveData reference:
```cs
using Gamekit2D.Runtime.Utils.SaveLoad;

private Saves.PlayerSaveData playerSaveData = new Saves.PlayerSaveData();
```
PlayerSaveData offers the following values to be set:
```cs
playerSaveData.position = new Vector2(5, 10);
playerSaveData.currentLevel = 1;
playerSaveData.health = 100f;
playerSaveData.xp = 10f;
```
<br><br>
## InventorySaveData
This is a preset class designed to make it easier to save common values attached to your inventory.

To create your own inventorySaveData reference:
```cs
using Gamekit2D.Runtime.Utils.SaveLoad;

private Saves.InventorySaveData inventorySaveData = new Saves.InventorySaveData();
```
To save an array of items into your inventorySaveData profile object:
```cs
using Gamekit2D.Runtime.Items;
using Gamekit2D.Runtime.Items.Profiles;

inventorySaveData.inventoryData = new Inventory(5)
  {
      items = new[]
      {
          new InventoryItemData {itemID = ScriptableObject.CreateInstance<MiscProfile>().itemID},
          new InventoryItemData {itemID = ScriptableObject.CreateInstance<MiscProfile>().itemID},
          new InventoryItemData {itemID = ScriptableObject.CreateInstance<MiscProfile>().itemID},
          new InventoryItemData {itemID = ScriptableObject.CreateInstance<MiscProfile>().itemID},
      }
  };
```
Of course, you can reference the items in your Inventory class instead.
<br><br>
## Custom Save Data
The Framework supports custom SaveData objects where you can set your own values. To define your own SaveData, simply create your own record that inherits the SaveData functionality:
```cs
using Gamekit2D.Runtime.Utils.SaveLoad;

[System.Serializable]
public record CustomSaveData : SaveProfileData
{
  public float myCustomValue1;
  public int myCustomValue2;
  public bool myCustomValue3;  
}
```
Then, create a reference:
```cs
private CustomSaveData myCustomSaveData = new CustomSaveData();
```
Then, you can set values:
```cs
myCustomSaveData.myCustomValue1 = 100f;
```

---

# Saving SaveData Objects
To save any SaveData, you can use the following line:
```cs
/*
saveName = The file name of the save. You will need this when loading the save.
overwrite = Automatically overwrite any saves that may have the same name. Otherwise, trying to overwrite a file will throw an Exception
encrypt = Encrypt the JSON string before writing the file. It is recommended you set this to True in production code. If the file is encrypted in saving, you MUST set this parameter to true when loading
*/
<saveDataObject>.SaveAs(string saveName, bool overwrite = false, bool encrypt = true);
```
For example:
```cs
playerSaveData.SaveAs("TestData", true, false);
```
The Framework also offers an [Async](https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/async-scenarios) variation of the SaveAs method:
```cs
playerSaveData.SaveAsAsync("TestData", true, false);
```

---

# Loading SaveData Objects
Before loading a save, you MUST ensure:
1. you are loading with the correct file name
2. the file actually exists
3. if the file is encrypted, make sure the file is being decrypted
4. the file is being deserialized into the correct SaveData object upon loading

To load a save, you can use the following line:
```cs
/*
profileName = The file name of the save. You will need this when loading the save. If the file does not exist, the function will throw an exception.
encryptionEnabled = Decrypt the JSON string before writing the file. It is recommended you set this to True in production code. If the file is encrypted in saving, you MUST set this parameter to true when loading
*/
var loadedData = SaveManager.LoadAs<<saveDataObject>>(string profileName, bool encryptionEnabled = true).data;
```
For example:
```cs
var loadedData = SaveManager.LoadAs<Saves.PlayerSaveData>("TestData", false);
```
The framework also offers an [Async](https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/async-scenarios) variation of the LoadAs method:
```cs
//If you are requiring data after it has been loaded, you should await this call.
var loadedData = SaveManager.LoadAsAsync<Saves.PlayerSaveData>("TestData", false);
```

---

# Deleting Saves
To delete a save, use the following line:
```cs
/*
profileName = the filename of the profile to be deleted. If the file does not exist, this function won't do anything
*/
SaveManager.DeleteSave(string profileName);
```
The framework also offers an [Async](https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/async-scenarios) variation of the DeleteSave method:
```cs
SaveManager.DeleteSaveAsync(string profileName);
```
