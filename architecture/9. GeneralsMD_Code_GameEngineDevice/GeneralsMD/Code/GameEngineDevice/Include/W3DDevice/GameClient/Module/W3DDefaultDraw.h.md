# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DDefaultDraw.h

## Purpose
Defines the default client update module for rendering W3D objects in the game engine.

## Responsibilities
- Provides default rendering behavior for game objects
- Manages shadows and shroud visibility
- Handles geometry and transform changes
- Implements module lifecycle via memory pool macros

## Key Types
- **W3DDefaultDraw (Class)**: Default client update module for rendering
- **W3DDefaultDrawMagicEnum (Enum)**: Not inferable
- **W3DDefaultDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DDefaultDraw()
- Purpose: Constructor for the default draw module
- Calls: None

### doDrawModule()
- Purpose: Main rendering function for the module
- Calls: None

### setShadowsEnabled()
- Purpose: Enables/disables shadows for the object
- Calls: None

### setFullyObscuredByShroud()
- Purpose: Sets whether the object is fully obscured by shroud
- Calls: None

### reactToTransformChange()
- Purpose: Handles changes to object transformation
- Calls: None

## Globals
- None

## Dependencies
- `Common/GameType.h`
- `Common/DrawModule.h`
- `Common/FileSystem.h`
- `Thing` (forward reference)
- `RenderObjClass` (forward reference)
- `FXList` (forward reference)
