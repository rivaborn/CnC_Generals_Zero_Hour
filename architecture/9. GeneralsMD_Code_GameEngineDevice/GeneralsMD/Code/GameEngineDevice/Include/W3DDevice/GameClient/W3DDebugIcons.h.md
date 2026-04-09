# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDebugIcons.h

## Purpose
Header for a debug utility class that renders large numbers of debug icons for pathfinding visualization.

## Responsibilities
- Manages debug icon rendering in the 3D world
- Handles allocation and compression of debug icon arrays
- Provides static method to add debug icons
- Implements RenderObjClass interface for rendering

## Key Types
- `W3DDebugIcons` (Class): Debug icon rendering utility inheriting from RenderObjClass
- `DebugIcon` (Struct): Internal debug icon representation (forward declared)
- `MAX_ICONS` (Enum): Maximum number of debug icons (100000)

## Key Functions
### `addIcon`
- Purpose: Adds a debug icon at specified position with given parameters
- Calls: Not inferable (implementation in .cpp)

### `Render`
- Purpose: Renders all debug icons
- Calls: Not inferable (implementation in .cpp)

### `allocateIconsArray`
- Purpose: Allocates memory for debug icon array
- Calls: Not inferable

### `compressIconsArray`
- Purpose: Compresses debug icon array
- Calls: Not inferable

## Globals
- `m_debugIcons` (DebugIcon*): Pointer to debug icon array
- `m_numDebugIcons` (Int): Current number of debug icons
- `m_vertexMaterialClass` (VertexMaterialClass*): Material for rendering icons

## Dependencies
- `rendobj.h` (RenderObjClass)
- `vertmaterial.h` (VertexMaterialClass)
- `Lib/BaseType.h` (Base types like Int, Real)
- `always.h` (Common includes)
