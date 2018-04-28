# Makehuman High Fidelity extensions

## Installation

1) Install MakeHuman from here: http://www.makehuman.org/download.php

2) Install the blender tools from that location (there are two separate installs, one for makehuman and one for blender)

Copy data/rigs/high_fidelity.mhskel and data/rigs/high_fidelity.thumb to the data/rigs subdirectory in your makehuman installation directory.

The makehuman skeleton is intended to be used with Menithal's Blender HiFi Addon, available here.
https://github.com/Menithal/Blender-Hifi-Addon.  Install that addon into blender as documented.

## Usage

Launch MakeHuman and create your avatar.

When you're ready to export, select the High Fidelity skeleton in the Pose/Animate -> Skeleton tab, and select Tpose in the Pose/Animate -> Pose tab.

Export the makehuman avatar in mhx2 format.

Import that file into blender.  When you select import, in the lower left, there will be an 'Import MHX2' submenu.  Check 'Override Exported Data', select the following settings:
   Import Human Type:  Base
   Helper Geometry:    Unchecked
   Offset:             Unchecked   
   Face Shapes:        Checked
   Leave the rest as default
   
Once the model has loaded, select the avatars skeleton in object mode.

Click the 'MakeHuman Avatar' button under the 'High Fidelity' tab.  This will adjust the specular, bone rotations, bone positions.

Export the avatar as fbx in the normal way and import the result into High Fidelity.  (Try using the fst export if you wish) 