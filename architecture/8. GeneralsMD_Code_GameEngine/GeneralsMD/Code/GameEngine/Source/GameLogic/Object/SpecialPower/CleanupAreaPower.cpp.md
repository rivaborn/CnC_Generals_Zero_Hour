# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CleanupAreaPower.cpp

## Purpose
Implements the CleanupAreaPower module, which manages cleanup hazard updates for objects like ambulances.

## Responsibilities
- Initializes cleanup power module data
- Parses INI configuration for cleanup parameters
- Executes cleanup power at specified location
- Handles serialization (Xfer) and CRC for network sync

## Key Types
- **CleanupAreaPowerModuleData (Class)**: Stores cleanup power configuration (e.g., movement range)
- **CleanupAreaPower (Class)**: Manages cleanup power logic and interaction with CleanupHazardUpdate

## Key Functions
### `doSpecialPowerAtLocation`
- Purpose: Activates cleanup power at a target location
- Calls: `getObject()`, `getCleanupAreaPowerModuleData()`, `findUpdateModule()`, `setCleanupAreaParameters()`

### `buildFieldParse`
- Purpose: Registers INI fields for cleanup power configuration
- Calls: `SpecialPowerModuleData::buildFieldParse()`

### `xfer`
- Purpose: Serializes/deserializes cleanup power state
- Calls: `SpecialPowerModule::xfer()`

## Globals
- **None**

## Dependencies
- `PreRTS.h`, `Player.h`, `ThingTemplate.h`, `Xfer.h`
- `CleanupAreaPower.h`, `CleanupHazardUpdate.h`, `Object.h`
- `SpecialPowerModule`, `MultiIniFieldParse`, `Xfer`, `Coord3D`, `NameKeyType`
