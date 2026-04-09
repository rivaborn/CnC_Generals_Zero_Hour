# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ConvertToHijackedVehicleCrateCollide.h

## Purpose
Defines a crate module that converts target vehicles to hijacked state and kills their drivers upon collision.

## Responsibilities
- Handles collision behavior for "terrorist" crates
- Validates target objects before execution
- Executes vehicle hijacking logic
- Provides module data for configuration

## Key Types
- **ConvertToHijackedVehicleCrateCollideModuleData (Class)**: Stores module configuration (range of effect)
- **ConvertToHijackedVehicleCrateCollide (Class)**: Implements crate collision behavior for vehicle hijacking
- **ConvertToHijackedVehicleCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object type

## Key Functions
### ConvertToHijackedVehicleCrateCollide()
- Purpose: Constructor for the crate collision module
- Calls: Not inferable

### isValidToExecute()
- Purpose: Determines if the crate can be applied to the target object
- Calls: Not inferable

### executeCrateBehavior()
- Purpose: Performs the actual vehicle hijacking and driver killing
- Calls: Not inferable

### isHijackedVehicleCrateCollide()
- Purpose: Identifies this as a hijacking crate type
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/Module.h` - Base module definitions
- `GameLogic/Module/CrateCollide.h` - Base crate collision module
- `Thing` class (forward reference) - Game object system
