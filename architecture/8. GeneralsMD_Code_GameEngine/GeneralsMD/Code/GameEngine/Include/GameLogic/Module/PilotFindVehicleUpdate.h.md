# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PilotFindVehicleUpdate.h

## Purpose
Defines a game logic module for handling wounded idle infantry finding healing units or structures.

## Responsibilities
- Manages pilot vehicle search behavior
- Tracks scan frames, range, and minimum health thresholds
- Implements object creation and update logic
- Scans for closest target vehicles

## Key Types
- **PilotFindVehicleUpdateModuleData (Class)**: Stores module configuration (scan frames, range, min health).
- **PilotFindVehicleUpdate (Class)**: Main update module handling pilot vehicle search logic.
- **PilotFindVehicleUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **ThingTemplate (Class)**: Forward reference to thing template.
- **WeaponTemplate (Class)**: Forward reference to weapon template.

## Key Functions
### PilotFindVehicleUpdateModuleData::buildFieldParse
- Purpose: Parses module data from configuration files.
- Calls: Not inferable.

### PilotFindVehicleUpdate::onObjectCreated
- Purpose: Handles object creation logic.
- Calls: Not inferable.

### PilotFindVehicleUpdate::update
- Purpose: Updates pilot vehicle search state.
- Calls: Not inferable.

### PilotFindVehicleUpdate::scanClosestTarget
- Purpose: Scans for the closest target vehicle.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Common/KindOf.h`
- `GameLogic/Module/UpdateModule.h`
- `ModuleData` (base class)
- `UpdateModule` (base class)
- `Thing` (forward reference)
- `Object` (forward reference)
