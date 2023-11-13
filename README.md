# 2D Gamekit Complete Documentation READ FIRST

<u>DO NOT MODIFY ANYTHING WITHIN THE PACKAGE FOLDER</u>.
The package was designed to only expose the code & features which should be edited. Changing anything else may cause unexpected behaviours and stop the package from working properly.

Basic setup documentation can be found below, refer to the following links for more detailed documentation.
 - Third party License info can be found in [Third Party Notices](Third%20Party%20Notices.md)
 - Recent changes can be viewed in the [Change Log](CHANGELOG.md).
 - For support, please contact <u>[erenp.business@gmail.com](https://erenp.business@gmail.com)</u>
<br><br>

>### What's inside?
>- This package contains ready-made assets & over 50 script components 
which you can easily drag & drop onto GameObjects. Every component has been set up to
automatically adjust relevant settings on the GameObject to reduce errors.
<br><br>
>- This package also contains dozens of custom editors and scene-visualising tools
to make your development process even more streamlined.
<br><br>
>- Custom toolbars & menus have been written to allow you to simply right click and add
template objects into your scene e.g. collectables, checkpoints & enemies.

## Setup
### Package Dependencies
The following packages are required to ensure this framework works correctly.
- `com.unity.2d.tilemap.extras`: "2.2.3"
- `com.unity.2d.pixel-perfect`: "5.0.1"
- `com.unity.2d.tilemap`: "1.0.0"
- `com.unity.2d.sprite`: "1.0.0"
- `com.unity.inputsystem`: "1.3.0"
- `com.unity.textmeshpro`: "3.0.6"
- `com.unity.nuget.newtonsoft-json`: "3.0.2"
- `com.unity.mathematics`: "1.2.6"

To install:
1. Go to Window > Package Manager
2. Press the `+` button and select 'Add Package by Name'
3. Enter the package name as shown above
4. Enter the package version as shown above
5. Press Add (may take a few minutes)
<br>

### Installation

Before you use the package, you should set a few things up to make sure everything works as intended! The steps have been documented below:
1. Go to Edit > Project Settings > Tags & Layers
2. On 'User Layer 6' type: "Standable"
3. Then, on 'User Layer 7' type: "Actor"
4. Your settings should look like this:
   ![alt text](/Docs/tagsLayers.png)
5. Then, Go to Edit > Project Settings > Physics 2D
6. Uncheck 'Queries Hit Triggers'
7. [Optional] Scroll down to the 'Layer Collision Matrix' dropdown
8. Make sure to uncheck 'Actor x Actor' collisions to stop actors (characters) from being able to push or bump into each other
9. Your settings should look like this:
    ![alt text](/Docs/physics2D.png)

## Gamekit Settings
To modify the global settings for the game kit you should go to: `Window > Eren's Gamekit > Gamekit Settings`
<br><br>
Here you can modify 
- Scene transition style
- Scene transition color
- Input system asset

For a quick link to the documentation use: `Window > Eren's Gamekit > Gamekit Manual`
<br>
It is recommended you join the Gamekit discord server in `Window > Eren's Gamekit > Gamekit Support Server`
<br> In case you need any assistance in using the kit 
or encounter any errors or would like to suggest improvements to the framework.
