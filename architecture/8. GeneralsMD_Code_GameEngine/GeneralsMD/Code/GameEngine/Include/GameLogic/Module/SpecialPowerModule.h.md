# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialPowerModule.h

## Purpose
Defines the interface and implementation for special power modules in the game, handling abilities like superweapons or unit-specific powers.

## Responsibilities
- Provides base class for special power modules
- Manages cooldown timers and readiness states
- Defines interface for power execution methods
- Handles audio events and science requirements

## Key Types
- **SpecialPowerModuleInterface (Class)**: Abstract interface for special power functionality
- **SpecialPowerModuleData (Class)**: Data container for module configuration
- **SpecialPowerModule (Class)**: Concrete implementation of special power module
- **SpecialPowerModuleMagicEnum (Enum)**: Not inferable (empty)
- **SpecialPowerModule_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### `isReady`
- Purpose: Check if special power is available
- Calls: None visible

### `doSpecialPower`
- Purpose: Execute the special power
- Calls: `initiateIntentToDoSpecialPower`, `triggerSpecialPower`

### `startPowerRecharge`
- Purpose: Begin cooldown timer
- Calls: None visible

### `markSpecialPowerTriggered`
- Purpose: Handle power activation events
- Calls: None visible

## Globals
- None

## Dependencies
- `Common/AudioEventRTS.h`
- `Common/Module.h`
- `Common/Science.h`
- `GameLogic/Module/BehaviorModule.h`
- Forward references: `Object`, `SpecialPowerTemplate`, `FieldParse`
