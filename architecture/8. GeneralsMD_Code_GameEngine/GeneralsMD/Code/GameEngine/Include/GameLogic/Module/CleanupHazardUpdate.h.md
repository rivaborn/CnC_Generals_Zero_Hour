# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CleanupHazardUpdate.h

## Purpose
Defines a game module for handling hazard cleanup targeting logic in Command & Conquer Generals.

## Responsibilities
- Manages targeting and firing of cleanup hazards
- Handles area-based cleanup scanning
- Provides module data for configuration
- Implements update loop for hazard cleanup behavior

## Key Types
- **CleanupHazardUpdateModuleData (Class)**: Stores module configuration (weapon slot, scan frames, scan range)
- **CleanupHazardUpdate (Class)**: Main update module handling hazard cleanup behavior
- **CleanupHazardUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **ThingTemplate (Class)**: Forward reference to thing template
- **WeaponTemplate (Class)**: Forward reference to weapon template

## Key Functions
### CleanupHazardUpdate::onObjectCreated
- Purpose: Initializes module when object is created
- Calls: Not inferable

### CleanupHazardUpdate::update
- Purpose: Main update loop for hazard cleanup behavior
- Calls: Not inferable

### CleanupHazardUpdate::scanClosestTarget
- Purpose: Finds closest target for cleanup
- Calls: Not inferable

### CleanupHazardUpdate::fireWhenReady
- Purpose: Fires cleanup weapon when ready
- Calls: Not inferable

### CleanupHazardUpdate::setCleanupAreaParameters
- Purpose: Configures cleanup area parameters
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/KindOf.h` (for KindOf types)
- `GameLogic/Module/UpdateModule.h` (base class)
- `ThingTemplate`, `WeaponTemplate` (forward references)
- `ModuleData` (base class for module data)
- `MultiIniFieldParse
