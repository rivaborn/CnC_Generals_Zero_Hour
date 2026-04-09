# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FirestormDynamicGeometryInfoUpdate.h

## Purpose
Defines a module for updating dynamic geometry with particle effects and damage in the Firestorm expansion.

## Responsibilities
- Extends `DynamicGeometryInfoUpdate` to add particle system effects
- Manages damage application to geometry
- Handles scorch mark placement
- Controls timing of effects and damage

## Key Types
- `MAX_FIRESTORM_SYSTEMS` (Enum): Maximum number of particle systems (16)
- `ParticleSystemTemplate` (Class): Reference to particle system templates
- `FirestormDynamicGeometryInfoUpdateModuleData` (Class): Module data containing particle system references and damage parameters
- `FirestormDynamicGeometryInfoUpdate` (Class): Main update module class
- `FirestormDynamicGeometryInfoUpdateMagicEnum` (Enum): Not inferable (likely internal macro enum)

## Key Functions
### `FirestormDynamicGeometryInfoUpdate::update`
- Purpose: Main update loop for the module
- Calls: `doDamageScan`

### `FirestormDynamicGeometryInfoUpdate::doDamageScan`
- Purpose: Applies damage to nearby objects based on module parameters
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/Geometry.h`
- `GameLogic/Module/DynamicGeometryInfoUpdate.h`
- `MultiIniFieldParse` (external)
- `FXList` (external)
- `ParticleSystemID` (external)
- `Thing` (external)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
