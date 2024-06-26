# Eren's 2D Framework Documentation

Basic setup documentation can be found below, refer to the following links for more detailed documentation.
 - Third party License info can be found in [Third Party Notices](Third%20Party%20Notices.md)
 - Recent changes can be viewed in the [Change Log](CHANGELOG.md).
 - For support, please contact <u>[erenp.business@gmail.com](https://erenp.business@gmail.com)</u>
 - Join Eren's Discord Server for latest changes, or logging an issue! [Discord Server](https://discord.com/invite/K4fQ6s82Q4)
<br><br>

> [!CAUTION]
> It is recommended you do not modify any code inside the package except in very specific circumstances. The package was designed to only expose the code & features which should be edited.
>
> Changing anything else may cause unexpected behaviours and stop the package from working properly.

> [!tip]
>### What's inside?
>- This package contains ready-made assets & over 100 script components 
which you can easily drag & drop onto GameObjects. Every component has been set up to
automatically adjust relevant settings on the GameObject to reduce errors.
<br><br>
>- This package also contains dozens of custom editors and scene-visualising tools
to make your development process even more streamlined.
<br><br>
>- Custom toolbars & menus have been written to allow you to simply right click and add
template objects into your scene e.g. collectables, checkpoints & enemies.

---

## Installation
### Package Dependencies
> [!TIP]
> To install:
> 1. Go to Window > Package Manager
> 2. Press the `+` button and select 'Add Package by Name'
> 3. Enter the package name as shown above
> 4. Enter the package version as shown above
> 5. Press Add (may take a few minutes)

The following packages are required to ensure this framework works correctly. The version of packages may vary depending on your Unity version.
| Package Name | Version |
|------|---------|
`com.unity.2d.tilemap.extras` | `2.2.3` |
| `com.unity.2d.pixel-perfect` | `5.0.1` | 
| `com.unity.2d.tilemap` | `1.0.0` | 
| `com.unity.2d.sprite` | `1.0.0` | 
| `com.unity.inputsystem` | `1.3.0` |
| `com.unity.textmeshpro` | `3.0.6` |
| `com.unity.nuget.newtonsoft-json` | `3.0.2`|
| `com.unity.mathematics` | `1.2.6` |
| `nuget.castle-core` | `1.0.1` |
| `com.unity.ext.nunit` | `1.0.6` |
| `nuget.moq` | `1.0.0` |
| `com.unity.test-framework` | `1.1.33` |

### Modify `Packages/manifest.json` 
> [!NOTE]
> - Because we want to create runtime tests, we need to make sure we can access our Input System from our tests. This is so we can simulate user input like Keyboard, Mouse or Gamepad from our tests to ensure our characters or UI behave properly

1. Navigate to your Unity Project's root folder, either via Windows Explorer or otherwise. You can also right click in your project window and select `Show in explorer`.
2. From the root folder, go to `/Packages`
3. Right click on `manifest.json` and select `Open with Notepad` (or your code editor of choice)
4. You should see the following contents (or similar)
```
{
  "dependencies": {
    "com.unity.ai.navigation": "1.1.1",
    "com.unity.feature.2d": "1.0.0",
    ...
  }
}
```
5. Append, the following chunk to your json so that it looks like this:
6. SAVE the file, close it, and return to Unity
```
{
  "dependencies": {
    "com.unity.ai.navigation": "1.1.1",
    "com.unity.feature.2d": "1.0.0",
    ...
  },
  "testables": [
    "com.unity.inputsystem"
  ]
}
```
> [!WARNING]
> 1. Make sure you have used the quotation marks "" in the correct places
> 2. Make sure you have used SQUARE BRACKETS
> 3. Make sure you have spelt the package name correctly
> 4. make sure you include the COMMA , after the closing curly brace of dependencies
> - When you go back into Unity, Unity will rebuild your packages. Should anything go wrong, go back to step 3. and ensure you have done everything correctly


---

## Setup and Configuration

Before you use the package, you should set a few things up to make sure everything works as intended! The steps have been documented below:
1. Go to Edit > Project Settings > Tags & Layers
2. On 'User Layer 6' type: "Standable"
3. Then, on 'User Layer 7' type: "Actor"
4. Your settings should look like this:
   ![alt text](/Resources/tagsLayers.png)
5. Then, Go to Edit > Project Settings > Physics 2D
6. Uncheck 'Queries Hit Triggers'
7. [Optional] Scroll down to the 'Layer Collision Matrix' dropdown
8. Make sure to uncheck 'Actor x Actor' collisions to stop actors (characters) from being able to push or bump into each other
9. Your settings should look like this:
    ![alt text](/Resources/physics2D.png)

### Framework Settings
To modify the global settings for the package you should go to: `Window > Eren's 2D Framework > Framework Settings`
<br><br>
Here you can modify 
- Scene transition style
- Scene transition color
- Scene transition speed

For a quick link to the documentation use: `Window > Eren's 2D Framework > Documentation`
<br>
It is recommended you join Eren's Official Discord server in `Window > Eren's 2D Framework > Discord`
<br> In case you need any assistance in using the package 
or encounter any errors or would like to suggest improvements to the framework.

---

## Bugs Reports and Feature Requests

In the event you encounter any bugs or have an idea for a new feature, head to the Issues tab in this repository and please create a new issue. Please provide as much information as possible and this will help me to help you!
