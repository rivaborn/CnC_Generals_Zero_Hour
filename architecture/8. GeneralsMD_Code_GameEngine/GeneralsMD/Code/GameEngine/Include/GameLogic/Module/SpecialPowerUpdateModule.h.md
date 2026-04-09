# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialPowerUpdateModule.h

## Purpose
Defines interfaces and base class for handling special power updates in the game engine.

## Responsibilities
- Declares `SpecialPowerUpdateInterface` with pure virtual methods for special power logic.
- Provides `SpecialPowerUpdateModule` base class implementing some interface methods.
- Manages memory allocation and module serialization macros.
- Defines science test and command option handling for special powers.

## Key Types
- **SpecialPowerUpdateInterface (Class)**: Interface for special power update functionality.
- **SpecialPowerUpdateModule (Class)**: Base module class implementing part of the interface.
- **SpecialPowerUpdateModuleMagicEnum (Enum)**: Not inferable (empty).
- **SpecialPowerUpdateModule_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty).

## Key Functions
### SpecialPowerUpdateModule()
- Purpose: Constructor for the module.
- Calls: Not inferable.

### doesSpecialPowerUpdatePassScienceTest()
- Purpose: Checks if special power passes science test.
- Calls: Not inferable.

### getExtraRequiredScience()
- Purpose: Returns extra required science type.
- Calls: Not inferable.

### initiateIntentToDoSpecialPower()
- Purpose: Initiates intent to use a special power (pure virtual).
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `Common/Module.h`
- `Common/GameType.h`
- `UpdateModule` (base class)
- `SpecialPowerTemplate`, `Object`, `Coord3D`, `Waypoint`, `CommandButton`, `CommandOption`, `ScienceType` (external types)
