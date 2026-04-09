# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDebugIcons.h

## Purpose
Header for a debug rendering system that draws pathfinding icons in the 3D world.

## Responsibilities
- Manages a pool of debug icons for visualization
- Handles rendering of debug icons in the scene
- Provides static methods to add debug icons
- Manages memory allocation for icon storage

## Key Types
- `W3DDebugIcons` (Class): Debug rendering system for pathfinding visualization
- `DebugIcon` (Struct): Not defined here, used for icon storage
- `MAX_ICONS` (Enum): Maximum number of debug icons (100000)

## Key Functions
### `addIcon`
- Purpose: Adds a debug icon to the rendering system
- Calls: Not inferable (implementation in .cpp)

### `allocateIconsArray`
- Purpose: Allocates memory for the debug icons array
- Calls: Not inferable

### `compressIconsArray`
- Purpose: Compresses the debug icons array
- Calls: Not inferable

## Globals
- `m_debugIcons` (DebugIcon*): Pointer to debug icons array
- `m_numDebugIcons` (Int): Current number of debug icons

## Dependencies
- `rendobj.h` (RenderObjClass)
- `vertmaterial.h` (VertexMaterialClass)
- `Lib/BaseType.h` (Base types like Int, Real)
- `always.h` (Common includes)
