# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectDefectionHelper.h

## Purpose
Manages object defection logic, including timers and visual effects for defecting units.

## Responsibilities
- Tracks defection timers and flashing phases
- Handles defection-related visual effects
- Provides disabled type filtering for defection processing
- Initializes and updates defection state

## Key Types
- **ObjectDefectionHelperModuleData (Class)**: Module data container for defection helper
- **ObjectDefectionHelper (Class)**: Core class handling defection logic
- **ObjectDefectionHelperMagicEnum (Enum)**: Not inferable
- **ObjectDefectionHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### ObjectDefectionHelper::update
- Purpose: Updates defection state and timers
- Calls: Not inferable

### ObjectDefectionHelper::getDisabledTypesToProcess
- Purpose: Returns disabled types to ignore during defection processing
- Calls: None

### ObjectDefectionHelper::startDefectionTimer
- Purpose: Starts the defection timer with optional visual effects
- Calls: None

## Globals
- **DEFECTION_DETECTION_TIME_MAX (const)**: Maximum defection detection time in logic frames

## Dependencies
- `GameLogic/Module/ObjectHelper.h`
- `ModuleData`, `Thing`, `DisabledMaskType`, `DISABLEDMASK_ALL` (external types)
- Memory pool macros and module macros (SAGE engine infrastructure)
