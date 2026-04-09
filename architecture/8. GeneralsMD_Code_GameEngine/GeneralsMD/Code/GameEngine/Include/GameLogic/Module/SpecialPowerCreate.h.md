# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialPowerCreate.h

## Purpose
Handles special power activation when a building is created in the game.

## Responsibilities
- Triggers special power countdowns on building creation
- Manages module lifecycle via CreateModule inheritance
- Implements build completion callback

## Key Types
- **Thing (Class)**: Base game object type this module attaches to
- **SpecialPowerCreate (Class)**: Module that handles special power creation logic
- **SpecialPowerCreateMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **SpecialPowerCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### SpecialPowerCreate()
- Purpose: Constructor for the module
- Calls: Not inferable (base class constructor likely called)

### onCreate()
- Purpose: Initialization callback when module is created
- Calls: Not inferable

### onBuildComplete()
- Purpose: Callback invoked when attached building finishes construction
- Calls: Not inferable

## Globals
- None

## Dependencies
- `CreateModule.h` (base class)
- `Thing` class (game object reference)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro system (`MAKE_STANDARD_MODULE_MACRO`)
