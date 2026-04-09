# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDebugIcons.cpp

## Purpose
Handles rendering of debug icons for pathfinding visualization in debug/internal builds.

## Responsibilities
- Manages a pool of debug icons with position, size, color, and lifetime
- Renders icons as textured quads with alpha blending
- Automatically purges expired icons
- Provides static helper function for adding icons

## Key Types
- `DebugIcon` (struct): Stores position, width, color, and end frame for a debug icon
- `W3DDebugIcons` (class): Main debug icon manager class inheriting from `RenderObjClass`

## Key Functions
### `addIcon`
- Purpose: Adds a new debug icon to the render queue
- Calls: `TheGameLogic->getFrame()`

### `Render`
- Purpose: Renders all active debug icons using dynamic vertex buffers
- Calls: `DX8Wrapper::Set_Material`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Transform`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Set_Index_Buffer`, `DX8Wrapper::Set_Vertex_Buffer`, `DX8Wrapper::Draw_Triangles`, `compressIconsArray()`

### `compressIconsArray`
- Purpose: Removes expired debug icons from the array
- Calls: `TheGameLogic->getFrame()`

## Globals
- `m_debugIcons` (DebugIcon*): Array storing active debug icons
- `m_numDebugIcons` (Int): Current count of active debug icons
- `m_vertexMaterialClass` (VertexMaterialClass*): Material used for rendering icons

## Dependencies
- `W3DDebugIcons.h`, `Common/GlobalData.h`, `GameLogic/GameLogic.h`, `Common/MapObject.h`, `WW3D2/DX8Wrapper.h`
- `RenderObjClass`, `VertexMaterialClass`, `ShaderClass`, `DynamicVBAccessClass`, `DynamicIBAccessClass`
- `TheGlobalData`, `TheGameLogic`
