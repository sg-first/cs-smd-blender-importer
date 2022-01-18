CS1.6 smd blender importer
=================

Installation
------------
Install this script as an add-on:

1. Open Blender's User Preferences window and go to the Add-ons tab.
2. Click Install from File `io_scene_studiomodel_import.py`.
3. Enable the Import-Export: Import SMD: Valve studiomodel source format addon.

Importing SMD Meshes
-------------
File | Import | Studiomodel Mesh Source

Importing SMD Animations(Not fixed)
---------------
1. Set the time slider to the frame you want the sequence to start at.
2. Select the armature that you want to add animation to or a mesh object deformed by that armature. The armature should match the skeleton in the file you are going to import.
3. Click File | Import | Studiomodel Animation Source in the main menu.

If everything is OK, the animation sequence is added, and markers are placed in the timeline for the start (`"<filename></filename>_start"`) and end (`"<filename></filename>_end"`) of the sequence.

### Notes
The importer transfers the keys defined in the .smd to the fcurves of the armature's bones. If your armature is rigged with constraints, drivers and IK, and those are enabled, don't expect the resulting animations to match those in the file. However, the keys will be there, so when you disable your extra rigging features at any time, you should have a faithful representation of the animation in the file.

For bone rotations, the importer sets keys on both the Euler and quaternion channels.
