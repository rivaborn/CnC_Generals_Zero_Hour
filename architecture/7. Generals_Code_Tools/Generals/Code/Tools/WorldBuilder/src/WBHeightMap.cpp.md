# Generals/Code/Tools/WorldBuilder/src/WBHeightMap.cpp

## Purpose
Handles rendering and collision detection for terrain in WorldBuilder, with support for flattening heights for top-down view.

## Responsibilities
- Renders terrain with optional height flattening
- Handles ray casting against terrain
- Provides height queries for terrain cells
- Manages vertex buffer updates for flattened terrain

## Key Types
- **WBHeightMap (Class)**: Terrain rendering and collision handling with flattening support
- **HeightMapRenderObjClass (Class)**: Base class for heightmap rendering (external)
- **DX8VertexBufferClass (Class)**: DirectX vertex buffer management (external)
- **RayCollisionTestClass (Class)**: Ray casting collision test (external)

## Key Functions
### `setFlattenHeights(Bool flat)`
- Purpose: Enables/disables terrain flattening and updates vertex buffers
- Calls: `updateBlock`

### `flattenHeights()`
- Purpose: Sets all terrain vertices to a fixed Z height for top-down view
- Calls: `DX8VertexBufferClass::WriteLockClass`

### `getMaxCellHeight(Real x, Real y)`
- Purpose: Returns maximum height of terrain cell containing given point
- Calls: `HeightMapRenderObjClass::getMaxCellHeight`

### `getHeightMapHeight(Real x, Real y, Coord3D* normal)`
- Purpose: Returns height and normal at given terrain coordinates
- Calls: `HeightMapRenderObjClass::getHeightMapHeight`

### `Cast_Ray(RayCollisionTestClass & raytest)`
- Purpose: Performs ray casting against flattened or normal terrain
- Calls: `HeightMapRenderObjClass::Cast_Ray`, `CollisionMath::Collide`

### `Render(RenderInfoClass & rinfo)`
- Purpose: Renders terrain with current flattening state
- Calls: `flattenHeights`, `HeightMapRenderObjClass::Render`

## Globals
- **THE_Z (const)**: Fixed Z height used for flattened terrain (10)

## Dependencies
- `WBheightmap.h`, `common/GlobalData.h`
- `tri.h`, `colmath.h`, `coltest.h`
- `HeightMapRenderObjClass`, `DX8VertexBufferClass`, `CollisionMath`
