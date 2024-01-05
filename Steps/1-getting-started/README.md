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

