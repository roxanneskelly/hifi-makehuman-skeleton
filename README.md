# Makehuman High Fidelity extensions

## Installation

1) Install MakeHuman from here: [Makehuman Download](http://www.makehuman.org/download.php)

2) Install [makehuman_plugins_for_1.1.1.zip](http://download.tuxfamily.org/makehuman/releases/1.1.1/makehuman_plugins_for_1.1.1.zip) as per instructions in  [README](http://download.tuxfamily.org/makehuman/releases/1.1.1/README.txt)

3) Install the [Blender plugins](http://download.tuxfamily.org/makehuman/releases/1.1.1/blender_plugins_for_1.1.1.zip) via the [blender add-on page](https://docs.blender.org/manual/en/dev/preferences/addons.html) 

4) Copy [data/rigs/high_fidelity.mhskel](https://raw.githubusercontent.com/roxanneskelly/hifi-makehuman-skeleton/master/data/rigs/high_fidelity.mhskel) and [data/rigs/high_fidelity.thumb](https://github.com/roxanneskelly/hifi-makehuman-skeleton/blob/master/data/rigs/high_fidelity.thumb?raw=true) to the data/rigs subdirectory in your makehuman installation directory.

5) The makehuman skeleton is intended to be used with Menithal's Blender HiFi Addon, available [here](https://github.com/Menithal/Blender-Hifi-Addon).  Install that addon into blender as documented.

6) Launch the MakeHuman binary from the install directory, go to the Community tab, and download any assets (clothing, etc.) that might be fun.

## Usage

1) Launch MakeHuman and create your avatar.

2) When you've built your avatar, pose it.  Select the High Fidelity skeleton in the Pose/Animate -> Skeleton tab, and select Tpose in the Pose/Animate -> Pose tab.

3) Export the makehuman avatar in mhx2 format.  Be sure to set the 'scale units' to 'meter', all other options should be default.

4) Import that file into blender.  When you select import, in the lower left, there will be an 'Import MHX2' submenu.  Check 'Override Exported Data', select the following settings:
   Import Human Type: Base, Helper Geometry: Unchecked, Offset: Checked, Face Shapes: Checked, Masking: Ignore.  Leave the rest as default
   
5) Once the model has loaded, select the avatars skeleton in object mode.

6) Click the 'MakeHuman Avatar' button under the 'High Fidelity' tab.  This will adjust the specular, bone rotations, bone positions.

7) Export the avatar as fbx in the normal way and import the result into High Fidelity.  (Try using the fst export if you wish)

8) Open your FST file and add the following to enable the blendshapes:

```
bs = JawOpen = mouth_open = 0.5
bs = MouthSmile_R = mouth_corner_in_right = 1
bs = MouthSmile_L = mouth_corner_in_left = 1
bs = LipsFunnel = tongue_up = 0.5
bs = LipsFunnel = mouth_narrow_right = 1
bs = LipsFunnel = mouth_narrow_left = 1
bs = LipsPucker = mouth_narrow_right = 1
bs = LipsPucker = mouth_narrow_left = 1
bs = LipsLowerDown = lips_mid_lower_down_right = 0.69999999999999996
bs = LipsLowerDown = lips_mid_lower_down_left = 0.69999999999999996
bs = LipsLowerClose = lips_lower_in = 1
bs = Puff = cheek balloon_right = 1
bs = Puff = cheek balloon_left = 1
bs = BrowsU_R = brow_outer_up_right = 1
bs = BrowsU_L = brow_outer_up_left = 1
bs = BrowsD_R = brow_outer_down_right = 1
bs = BrowsD_L = brow_outer_down_left = 1
bs = BrowsU_C = brow_mid_up_right = 0.5
bs = BrowsU_C = brow_mid_up_left = 0.5
bs = EyeBlink_L = EyeBlink_L = 1
bs = EyeBlink_R = EyeBlink_R = 1
```
