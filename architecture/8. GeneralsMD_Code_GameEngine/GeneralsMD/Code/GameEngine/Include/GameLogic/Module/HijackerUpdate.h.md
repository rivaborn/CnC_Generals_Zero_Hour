# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HijackerUpdate.h

## Purpose
Defines the HijackerUpdate module for managing hijacker behavior when attached to a vehicle.

## Responsibilities
- Tracks hijacker attachment to a vehicle via bone
- Manages hijacker ejection when vehicle is destroyed
- Handles parachute deployment post-ejection
- Controls update cycles for hijacker state

## Key Types
- **HijackerUpdateModuleData (Class)**: Stores module configuration (bone attachment, parachute name)
- **HijackerUpdate (Class)**: Implements hijacker vehicle attachment logic
- **HijackerUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **HijackerUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### HijackerUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data
- Calls: UpdateModuleData::buildFieldParse

### HijackerUpdate::update
- Purpose: Updates hijacker state (attachment/ejection logic)
- Calls: Not inferable (implementation in .cpp)

### HijackerUpdate::setTargetObject
- Purpose: Sets the vehicle the hijacker is attached to
- Calls: None

### HijackerUpdate::getTargetObject
- Purpose: Retrieves the attached vehicle
- Calls: None

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (INI parsing)
- AsciiString (string handling)
- ObjectID, Coord3D (game object types)
