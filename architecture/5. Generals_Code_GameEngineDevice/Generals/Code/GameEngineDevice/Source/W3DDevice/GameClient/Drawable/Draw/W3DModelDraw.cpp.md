# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DModelDraw.cpp

## Purpose
Handles 3D model rendering and animation logic for the SAGE engine, including state management, bone manipulation, and weapon effects.

## Responsibilities
- Manages W3D model rendering and animation states
- Handles bone transformations and sub-object visibility
- Processes weapon recoil and projectile effects
- Parses model condition states from INI files
- Serializes/deserializes model state for save/load

## Key Types
- `INIReadFlagsType` (Enum): Flags for INI parsing state
- `ACBits` (Enum): Animation control bit flags
- `ParseCondStateType` (Enum): Condition state parsing modes
- `AnimParseType` (Enum): Animation parsing types
- `W3DAnimationInfo` (Class): Stores animation metadata
- `ModelConditionInfo` (Class): Manages model condition states

## Key Functions
### `isValidTimeToCalcLogicStuff`
- Purpose: Checks if logic calculations are safe to perform
- Calls: `TheGameLogic->isInGameLogicUpdate()`, `TheGameState->isInLoadGame()`

### `parseAnimation`
- Purpose: Parses animation data from INI files
- Calls: `parseAsciiStringLC`, `parseRealRange`, `parseLowercaseNameKey`

### `doHideShowBoneSubObjs`
- Purpose: Recursively hides/shows bone sub-objects
- Calls: `m_renderObject->Get_Sub_Object_Bone_Index()`, `subObj->Set_Hidden()`

### `updateSubObjects`
- Purpose: Updates visibility of sub-objects based on current state
- Calls: `m_renderObject->Get_Sub_Object_By_Name()`, `subObj->Set_Hidden()`

### `xfer`
- Purpose: Serializes/deserializes model state
- Calls: `DrawModule::xfer()`, `xfer->xferVersion()`, `xfer->xferBool()`

## Globals
- `ACBitsNames` (const char*): Array of animation control bit names
- `ALL_MAINTAIN_FRAME_FLAGS` (Int): Bitmask of maintain frame flags
- `TerrainDecalTextureName` (char*): Terrain decal texture names
- `NO_NEXT_DURATION` (UnsignedInt): Special duration value

## Dependencies
- Common game systems (CRC, GameState, RandomValue)
- W3D rendering system (HAnim, HLod, RendObj)
- Game logic (GameLogic, Object, WeaponSet)
- Serialization (Xfer)
- Debug utilities (CRCDebug, PerfTimer)
