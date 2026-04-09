# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DynamicGeometryInfoUpdate.cpp

## Purpose
Handles dynamic updates to an object's geometry (height and radii) over time.

## Responsibilities
- Manages interpolation between initial and final geometry values
- Supports optional reversal at transition time
- Handles initial delay before starting the update
- Serializes/deserializes update state for networking

## Key Types
- `DynamicGeometryInfoUpdateModuleData` (Class): Stores configuration for the update (delays, initial/final values, transition time)
- `DynamicGeometryInfoUpdate` (Class): Implements the update logic
- `GeometryInfo` (Class): Represents object geometry (referenced but not defined here)

## Key Functions
### `DynamicGeometryInfoUpdate::update`
- Purpose: Interpolates geometry values over time and applies them to the object
- Calls: `getDynamicGeometryInfoUpdateModuleData`, `getObject`, `setGeometryInfo`

### `DynamicGeometryInfoUpdate::xfer`
- Purpose: Serializes/deserializes the update state for networking
- Calls: `UpdateModule::xfer`, `xferUnsignedInt`, `xferBool`, `xferReal`, `xferUser`

### `DynamicGeometryInfoUpdateModuleData::buildFieldParse`
- Purpose: Defines INI field parsing for module data
- Calls: `ModuleData::buildFieldParse`, `add`

## Globals
None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Module/DynamicGeometryInfoUpdate.h`, `GameLogic/Object.h`
- `INI`, `MultiIniFieldParse`, `Xfer`, `UpdateModule`, `Thing`, `ModuleData`, `GeometryInfo`
