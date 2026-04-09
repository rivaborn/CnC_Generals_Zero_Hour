# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HordeUpdate.h

## Purpose
Defines the HordeUpdate module for managing group behavior in the game, tracking "horde" status based on unit proximity and count.

## Responsibilities
- Manages horde membership logic for units
- Handles flag visibility based on horde status
- Provides interface for querying horde-related properties
- Updates horde status periodically

## Key Types
- **HordeActionType (Enum)**: Defines horde action types (only HORDEACTION_HORDE currently).
- **HordeUpdateModuleData (Class)**: Configuration data for horde behavior (update rate, kindof mask, min count/dist, etc.).
- **HordeUpdateInterface (Class)**: Abstract interface for horde-related queries.
- **HordeUpdate (Class)**: Main module implementing horde logic and update behavior.

## Key Functions
### HordeUpdate::update
- Purpose: Updates horde status based on nearby units.
- Calls: joinOrLeaveHorde, showHideFlag

### HordeUpdate::joinOrLeaveHorde
- Purpose: Adjusts horde membership based on iterator results.
- Calls: Not inferable

### HordeUpdate::showHideFlag
- Purpose: Shows/hides horde flag based on status.
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `Common/KindOf.h` (for KindOfMaskType)
- `SimpleObjectIterator` (forward declared)
- `UpgradeTemplate` (forward declared)
- `ModuleData` (base class for HordeUpdateModuleData)
