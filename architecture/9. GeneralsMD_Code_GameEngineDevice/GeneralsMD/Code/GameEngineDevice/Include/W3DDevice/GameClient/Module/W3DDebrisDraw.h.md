# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DDebrisDraw.h

## Purpose
Header for the W3DDebrisDraw class, which handles rendering of debris objects in the game.

## Responsibilities
- Manages debris rendering using W3D (W3D engine)
- Handles animation states (initial, flying, final)
- Controls shadows for debris objects
- Implements DebrisDrawInterface for debris drawing functionality

## Key Types
- **W3DDebrisDraw (Class)**: Main class for debris rendering
- **AnimStateType (Enum)**: Defines animation states (INITIAL, FLYING, FINAL)
- **Thing (Class)**: Forward reference to game object
- **RenderObjClass (Class)**: W3D render object
- **HAnimClass (Class)**: Animation class
- **Shadow (Class)**: Shadow rendering
- **FXList (Class)**: Effects list

## Key Functions
### W3DDebrisDraw()
- Purpose: Constructor for W3DDebrisDraw
- Calls: Not inferable

### doDrawModule()
- Purpose: Main draw method for debris rendering
- Calls: Not inferable

### setShadowsEnabled()
- Purpose: Enables/disables shadows for debris
- Calls: Not inferable

### setModelName()
- Purpose: Sets the model name and color for debris
- Calls: Not inferable

### setAnimNames()
- Purpose: Sets animation names for different states
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/GameType.h
- Common/DrawModule.h
- Common/FileSystem.h
- Forward references: Thing, RenderObjClass, HAnimClass, Shadow, FXList
