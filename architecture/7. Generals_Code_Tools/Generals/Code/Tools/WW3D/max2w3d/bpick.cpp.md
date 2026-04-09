# Generals/Code/Tools/WW3D/max2w3d/bpick.cpp

## Purpose
Implements a bone picker utility for 3DS Max, used to select bones in a skeleton hierarchy.

## Responsibilities
- Filters nodes to determine if they are valid bones
- Handles hit testing and picking of bones in the 3DS Max viewport
- Notifies the owning skin modifier when a bone is picked
- Provides dialog title and button text for the picker UI

## Key Types
- **BonePickerClass (Class)**: Main bone picker implementation
- **TheBonePicker (BonePickerClass)**: Global instance of the bone picker

## Key Functions
### `BonePickerClass::Filter`
- Purpose: Determines if a node is a valid bone
- Calls: None

### `BonePickerClass::HitTest`
- Purpose: Performs hit testing in the 3DS Max viewport
- Calls: `ip->PickNode`, `GetFilter`

### `BonePickerClass::Pick`
- Purpose: Handles the bone picking logic and notifies the user
- Calls: `vpt->GetClosestHit`, `User->User_Picked_Bone`

### `BonePickerClass::proc`
- Purpose: Processes a list of picked bones
- Calls: `User->User_Picked_Bones`

## Globals
- **TheBonePicker (BonePickerClass)**: Global instance of the bone picker

## Dependencies
- `bpick.h`, `dllmain.h`, `resource.h`
- `INode`, `IObjParam`, `ViewExp`, `ObjectState`, `INodeTab` (3DS Max SDK types)
- `Get_String` (resource string lookup)
