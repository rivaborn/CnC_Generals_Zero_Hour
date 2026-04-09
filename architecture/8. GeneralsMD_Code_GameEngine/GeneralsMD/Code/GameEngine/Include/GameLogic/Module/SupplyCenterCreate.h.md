# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyCenterCreate.h

## Purpose
Handles creation logic for Supply Centers, updating resource management when a new Supply Center is built.

## Responsibilities
- Manages Supply Center creation events
- Updates resource brains for all players when a Supply Center is created
- Handles build completion logic for Supply Centers
- Inherits from CreateModule for base functionality

## Key Types
- **SupplyCenterCreate (Class)**: Module for Supply Center creation logic
- **SupplyCenterCreateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **SupplyCenterCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Reference to game object being created

## Key Functions
### SupplyCenterCreate()
- Purpose: Constructor for SupplyCenterCreate module
- Calls: Not inferable (constructor body not shown)

### onCreate()
- Purpose: Handles creation event for Supply Center
- Calls: Not inferable (implementation not shown)

### onBuildComplete()
- Purpose: Called when Supply Center build is finished
- Calls: Not inferable (implementation not shown)

## Globals
- None

## Dependencies
- `CreateModule.h` (base class)
- `Thing` class (game object reference)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macros (`MAKE_STANDARD_MODULE_MACRO`)
