# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CleanupAreaPower.h

## Purpose
Defines the CleanupAreaPower module, which extends cleanup range until no hazards remain.

## Responsibilities
- Extends cleanup range dynamically
- Manages cleanup hazard removal
- Implements special power behavior
- Handles module data parsing

## Key Types
- **CleanupAreaPowerModuleData (Class)**: Holds module configuration (cleanup range)
- **CleanupAreaPower (Class)**: Implements the cleanup power logic
- **CleanupAreaPowerMagicEnum (Enum)**: Not inferable
- **CleanupAreaPower_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### CleanupAreaPowerModuleData::buildFieldParse
- Purpose: Parses module data from INI files
- Calls: Not inferable

### CleanupAreaPower::doSpecialPowerAtLocation
- Purpose: Executes cleanup power at specified location
- Calls: Not inferable

## Globals
- None

## Dependencies
- SpecialPowerModule.h
- MultiIniFieldParse (external)
- MemoryPoolObject (external)
- Thing (external)
- Coord3D (external)
