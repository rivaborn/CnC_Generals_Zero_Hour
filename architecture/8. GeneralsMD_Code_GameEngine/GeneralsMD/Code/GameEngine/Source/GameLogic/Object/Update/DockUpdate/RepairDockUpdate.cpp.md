# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/RepairDockUpdate.cpp

## Purpose
Handles the repair logic when a unit docks with a repair structure in the game.

## Responsibilities
- Manages health restoration for docked units
- Calculates health increment per frame based on repair time
- Handles docking process completion when repair is done
- Serializes repair state for networking

## Key Types
- **RepairDockUpdateModuleData (Class)**: Stores repair configuration (time for full heal)
- **RepairDockUpdate (Class)**: Implements repair docking behavior

## Key Functions
### RepairDockUpdate::action
- Purpose: Applies healing to docked unit each frame
- Calls: `getRepairDockUpdateModuleData`, `getBodyModule`, `attemptHealing`

### RepairDockUpdate::xfer
- Purpose: Serializes repair state for networking
- Calls: `DockUpdate::xfer`, `xferObjectID`, `xferReal`

## Globals
- None

## Dependencies
- `DockUpdate.h` (base class)
- `BodyModule.h` (for health management)
- `Xfer.h` (serialization)
- `Common/Xfer.h` (networking utilities)
