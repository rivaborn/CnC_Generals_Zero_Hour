# Generals/Code/Tools/WW3D/max2w3d/bpick.cpp - Enhanced Analysis

## Architectural Role
This file implements a 3DS Max plugin utility for bone selection, bridging the asset pipeline between Max and the W3D (Westwood 3D) format used by the game engine. It handles viewport interaction for skeleton editing, critical for character and unit animation assets.

## Cross-References
### Incoming
- Likely called by Max plugin infrastructure (e.g., modifier dialogs) when bone selection is initiated
- `User` (skin modifier) invokes `User_Picked_Bone`/`User_Picked_Bones` after picking

### Outgoing
- Calls 3DS Max SDK functions (`INode::EvalWorldState`, `IObjParam::PickNode`, `ViewExp::GetClosestHit`)
- Uses `Get_String` from `resource.h` for localized UI text

## Design Patterns
- **Singleton**: `TheBonePicker` global instance ensures one picker per Max session
- **Observer**: Notifies `User` (skin modifier) of picks via callback (`User_Picked_Bone`/`User_Picked_Bones`)
- **Strategy**: `Filter` encapsulates node validation logic, allowing dynamic bone list filtering

*Not inferable*: No clear use of Factory, Decorator, or Visitor patterns.
