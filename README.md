# BlenderAe Documentation (version 1.3.4)

BlenderAe is available here:
<https://aescripts.com/blenderae/>
<https://blendermarket.com/products/blenderae>

[For video tutorials click here](https://www.youtube.com/playlist?list=PL1c22fXzadmmcuGD6p-rCM_YXmwa21t7M)

## What is BlenderAe?

BlenderAe is a Blender addon that enables bidirectional data transfer between Blender and After Effects. Connect, select and export data from Blender to After Effects, or import layers from After Effects to Blender!

## What data does BlenderAe currently support?

### From Blender to After Effects

Object Mode:

1. Cameras to After Effects Cameras.
2. Lights.
3. Object transformations to Nulls.
4. Empty transformations to Nulls.
5. Planes (planar) to precomposed shape layers.

Edit Mode:

1. Selected vertices locations converted to Nulls.
2. Selected planar faces converted to precomposed shape layers.

<!-- Pose Mode:

1. Selected bones (heads and tails) converted to Nulls. -->

### From After Effects to Blender

1. Nulls to Empty objects.
2. Solids to Planes.
3. Cameras to Blender Cameras (including point of interest).
4. Experimental support for parented layers.

## How do I install BlenderAe?

Please follow the ffficial Blender addon installation documentation: <https://docs.blender.org/manual/en/latest/editors/preferences/addons.html>

BlenderAe is a Blender addon with no additional scripts to install for After Effects by default.

1. Go to 'Edit > Preferences > Addons'.
2. Click 'Install...'.
3. Select the 'BlenderAe.zip' and enable the checkbox to activate BlenderAe.

### Install dependencies

BlenderAe includes dependencies that help BlenderAe connect to After Effects more reliably. To install these dependencies, follow these steps:

1. Go to 'Edit > Preferences > Addons'.
2. Click 'Install Dependencies' in the BlenderAe addon panel.

[Here's a video tutorial on how to install BlenderAe](https://www.youtube.com/watch?v=1MFuTjgDnFs&list=PL1c22fXzadmmcuGD6p-rCM_YXmwa21t7M&index=2)

## How to use BlenderAe

### Connecting to After Effects

1. Open Adobe After Effects before clicking the "Connect to Ae" button.
2. The button will automatically search for the active After Effects path. Alternatively, manually add the path to the After Effects application file (e.g., "C:\Program Files\Adobe\Adobe After Effects 2023\Support Files\AfterFX.exe").
3. The "Use Ae Comp Center" checkbox centers exported objects in relation to the After Effects composition center.
4. The "Export Scale" value slider modifies the scale of the scene data for cases where you desire smaller or larger values in After Effects.
5. Click "Export to Ae" to transfer selected objects, vertices, or faces directly to After Effects.
6. The "Import Ae Layers" button imports Adobe After Effects orientation, rotation, position, and scale data into Blender for selected layers.
7. The "Import Scale" value slider modifies the scale of the scene data between After Effects and Blender.

### Manual Export and Import

1. To export data when After Effects is not connected, select and export object data to create a "BlenderAe" folder with the data file and a script file in the user's "Documents" folder.
2. In After Effects, go to "File > Scripts > Run Script File..." and select the script file located in the BlenderAe folder.

### Notes, Tips, and Known Issues

- A large number of selections or long frame duration can take a long time to process (face selection currently takes the longest amount of time to process).
- After Effects may appear frozen during processing.
- Non-planar Faces (in Edit Mode) and non-planar Planes (in Object Mode) are not currently supported as shape layers.
- Multiple vertex or face selections are supported for individual objects only (not across multiple object selections in Edit Mode).
- If the "Ae Path" field contains a correct path but After Effects is not open, After Effects will open and close without saving.
- Apply all modifiers and transforms to objects before exporting vertices or faces.
- When exporting data from Blender, the After Effects application window resizes out of fullscreen mode. To prevent this, use the "Maximize App Window" shortcut "CTRL + " instead.
