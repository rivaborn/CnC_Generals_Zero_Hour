# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DDebrisDraw.h

## Purpose
Defines the W3DDebrisDraw class for rendering debris objects in the game.

## Responsibilities
- Manages debris rendering using W3D (W3D engine)
- Handles animation states (initial, flying, final)
- Controls shadow rendering for debris
- Implements DebrisDrawInterface for debris drawing functionality

## Key Types
- W3DDebrisDraw (Class): Main debris rendering class
- AnimStateType (Enum): Animation state types (INITIAL, FLYING, FINAL)
- Thing (Class): Forward reference to game object
- RenderObjClass (Class): W3D render object
- HAnimClass (Class): Animation class
- Shadow (Class): Shadow rendering class
- FXList (Class): Effects list

## Key Functions
### doDrawModule
- Purpose: Renders the debris object
- Calls: Not inferable (implementation in .cpp)

### setShadowsEnabled
- Purpose: Enables/disables shadow rendering
- Calls: Not inferable

### setModelName
- Purpose: Sets the model name and color for debris
- Calls: Not inferable

### setAnimNames
- Purpose: Sets animation names for different states
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/GameType.h
- Common/DrawModule.h
- Common/FileSystem.h
- DrawModule base class
- DebrisDrawInterface interface
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macros (MAKE_STANDARD_MODULE_MACRO)
