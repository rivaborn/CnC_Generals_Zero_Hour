# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DModelDraw.cpp

## Purpose
Handles 3D model rendering and animation logic for the W3D (Westwood 3D) engine in Command & Conquer Generals.

## Responsibilities
- Manages model animations, states, and transitions
- Handles weapon recoil and projectile visibility
- Processes model condition states (e.g., carrying supplies)
- Supports serialization/deserialization of model data
- Manages sub-object visibility (e.g., turrets, weapons)

## Key Types
- `INIReadFlagsType` (Enum): Flags for INI parsing state
- `ACBits` (Enum): Animation control bit flags
- `ParseCondStateType` (Enum): Model condition state parsing modes
- `AnimParseType` (Enum): Animation parsing types
- `W3DAnimationInfo` (Class): Stores animation metadata
- `ModelConditionInfo` (Class): Manages model condition states

## Key Functions
### `isValidTimeToCalcLogicStuff`
- Purpose: Checks if it's safe to perform logic calculations
- Calls: `TheGameLogic->isInGameLogicUpdate()`, `TheGameState->isInLoadGame()`

### `parseAnimation`
- Purpose: Parses animation data from INI files
- Calls: `parseAsciiStringLC`, `parseRealRange`, `parseLowercaseNameKey`

### `doHideShowBoneSubObjs`
- Purpose: Recursively hides/shows bone sub-objects
- Calls: `m_renderObject->Get_Sub_Object_Bone_Index()`, `subObj->Set_Hidden()`

### `updateSubObjects`
- Purpose: Updates visibility of sub-objects based on current state
- Calls: `m_renderObject->Get_Sub_Object_By_Name()`, `doHideShowBoneSubObjs()`

### `xfer`
- Purpose: Serializes/deserializes model draw module data
- Calls: `DrawModule::xfer()`, `xfer->xferVersion()`, `xfer->xferBool()`

## Globals
- `ACBitsNames` (const char*): Array of animation control bit names
- `ALL_MAINTAIN_FRAME_FLAGS` (Int): Bitmask of maintain-frame flags
- `TerrainDecalTextureName` (char*): Terrain decal texture names
- `NO_NEXT_DURATION` (UnsignedInt): Invalid duration value

## Dependencies
- `Common/CRC.h`, `Common/GameState.h`, `GameClient/Drawable.h`
- `WW3D2/HAnim.h`, `WW3D2/RendObj.h`, `WW3D2/MeshMdl.h`
- `W3DDevice/GameClient/W3DAssetManager.h`, `W3DDevice/GameClient/W3DDisplay.h`
