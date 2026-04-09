# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PreorderCreate.h

## Purpose
Handles setting preorder status when a building is created in the game.

## Responsibilities
- Manages preorder creation logic for buildings
- Implements module lifecycle hooks (onCreate, onBuildComplete)
- Inherits from CreateModule base class
- Uses memory pool allocation for instances

## Key Types
- **PreorderCreate (Class)**: Module for handling preorder building creation
- **PreorderCreateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **PreorderCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Reference to game entity being created

## Key Functions
### PreorderCreate::PreorderCreate
- Purpose: Constructor for PreorderCreate module
- Calls: Not inferable (constructor body not shown)

### PreorderCreate::onCreate
- Purpose: Called when the module is created
- Calls: Not inferable

### PreorderCreate::onBuildComplete
- Purpose: Called when building construction is complete
- Calls: Not inferable

## Globals
- None

## Dependencies
- `CreateModule.h` (base class)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro system (`MAKE_STANDARD_MODULE_MACRO`)
- `Thing` class reference
