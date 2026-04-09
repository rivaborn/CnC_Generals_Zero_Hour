# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MissileLauncherBuildingUpdate.h

## Purpose
Defines a module for updating missile launcher building states during special power activation.

## Responsibilities
- Manages door state transitions (opening/closing) for missile launcher buildings
- Handles special power template integration
- Controls audio and visual effects for door states
- Provides special power update interface

## Key Types
- **MissileLauncherBuildingUpdateModuleData (Class)**: Holds configuration data for door timings and effects
- **MissileLauncherBuildingUpdate (Class)**: Main update module for missile launcher building states
- **DoorStateType (Enum)**: Represents door states (closed, opening, open, waiting, closing)

## Key Functions
### MissileLauncherBuildingUpdateModuleData::buildFieldParse
- Purpose: Parses INI configuration fields for module data
- Calls: UpdateModuleData::buildFieldParse

### MissileLauncherBuildingUpdate::update
- Purpose: Updates door state and handles special power logic
- Calls: Not inferable (implementation in .cpp)

### MissileLauncherBuildingUpdate::switchToState
- Purpose: Transitions between door states
- Calls: Not inferable (implementation in .cpp)

## Globals
None

## Dependencies
- Common/AudioEventRTS.h
- Common/INI.h
- GameLogic/Module/SpecialPowerUpdateModule.h
- DamageInfo, SpecialPowerTemplate, SpecialPowerModule, FXList (forward declarations)
