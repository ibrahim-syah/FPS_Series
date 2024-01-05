# Part 1: Getting Started

## Project Setup

Create a new UE4 project from the First Person Shooter template. Delete all vr related input, the "TurnRate" and "LookUpRate". Rename "Turn" to "LookRight". Add FireAxis mapping with left mouse button. Finally, remove motion blur.

If you try in PIE you will notice that you can't turn left or right, this is because we just renamed the "Turn" input.

## Animation Setup

Create "MyStuff" folder in "Content" and also "Animations" folder within "MyStuff". Then just drag and drop the contents of "FirstPerson" folder into the "Animations" folder in the content browser. When prompted, select the SK_Mannequin_Arms_Skeleton as the skeleton, then click "Import All".

Open all the imported animation and change each of their rate scale according to the following values:

- FP_Equip: 3.0
- FP_Fire: 3.0
- FP_Grenade: 3.0
- FP_Idle: 0.5
- FP_Inspect: 3.0
- FP_Inspect_2: 2.0
- FP_Melee: 2.0
- FP_Reload: 3.5
- FP_Stow: 4.0

Rate scale is pretty straightforward, it tweaks the playback rate of the animation.

Next, create an animation montage from all one-shot animations (everything except FP_Idle). For each of these montage, set each one to play in the "Arms" montage slot. Don't worry if you see the animation T-posing, you can save it, preview other animation, and go back to the montage and it'll work again. I don't know why it T-pose in the first place tho.

You need to set these sweet spot for montage blend in/out:

| Montage      | Blend in     | Blend out |
|--------------|-----------|------------|
| FP_Equip_Montage | 0.00  | 0.25        |
| FP_Fire_Montage      | 0.01  | 0.40       |
| FP_Grenade_Montage | 0.10 | 0.25 |
| FP_Inspect_Montage | 0.25 | 0.25 |
| FP_Inspect_2_Montage | 0.25 | 0.25 |
| FP_Melee_Montage | 0.10 | 0.25 |
| FP_Reload_Montage | 0.10 | 0.25 |
| FP_Stow_Montage | 0.25 | 0.00 |


I think this blend in/out values are used for smooth transition between one montage to the other.

Next, create a folder called Skeletons in MyStuff and within it, import the SK_Camera.fbx asset. This custom skeleton will be used for procedural camera animation later on. Ignore any warning that says the bone size is too small.

Open the imported skeleton asset and set the Character > Bones > All Hierarchy.