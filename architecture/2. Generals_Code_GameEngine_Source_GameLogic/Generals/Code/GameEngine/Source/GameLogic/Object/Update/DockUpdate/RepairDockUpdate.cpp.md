# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/RepairDockUpdate.cpp

## Purpose
This file implements the logic for repairing objects when they dock with a repair structure in Command & Conquer Generals.

## Responsibilities
- Handles the docking process and repairs the object over time.
- Manages the health addition per frame based on the module data.
- Ensures the docking process continues until the object is fully repaired or completes if no more healing is needed.

## Key Types
- `RepairDockUpdateModuleData (struct)`: Stores configuration for repair dock updates, such as frames required for full healing.
- `RepairDockUpdate (class)`: Manages the repair action during docking.

## Key Functions
### RepairDockUpdate::action
- Purpose: Performs the repair action while docked.
- Calls:
  - `getBodyModule()`
  - `getMaxHealth()`
  - `getHealth()`
  - `attemptHealing()`

### RepairDockUpdate::crc
- Purpose: Calculates the CRC for the object.
- Calls:
  - `DockUpdate::crc()`

### RepairDockUpdate::xfer
- Purpose: Handles serialization and deserialization of the object.
- Calls:
  - `DockUpdate::xfer()`
  - `xferObjectID()`
  - `xferReal()`

### RepairDockUpdate::loadPostProcess
- Purpose: Performs post-load processing.
- Calls:
  - `DockUpdate::loadPostProcess()`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/RepairDockUpdate.h"
