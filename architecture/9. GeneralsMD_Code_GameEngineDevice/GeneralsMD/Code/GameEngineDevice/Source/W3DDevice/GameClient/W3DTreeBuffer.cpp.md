# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DTreeBuffer.cpp

## Purpose
Manages rendering and behavior of trees in the 3D scene, including culling, sway animation, and toppling physics.

## Responsibilities
- Tree visibility culling and sorting
- Tree sway animation based on wind/breeze data
- Tree toppling physics (falling, bouncing, sinking)
- Tree texture atlas generation and rendering
- Network synchronization via Xfer system

## Key Types
- `(anonymous enum)` (Enum): Topple behavior flags (W3D_TOPPLE_OPTIONS_NONE, W3D_TOPPLE_OPTIONS_NO_BOUNCE, W3D_TOPPLE_OPTIONS_NO_FX)
- `W3DTreeTextureClass` (Class): Custom texture class for tree atlases
- `GDIFileStream2` (Class): File stream wrapper (truncated in output)

## Key Functions
### `W3DTreeBuffer::cull`
- Purpose: Marks trees visible/invisible based on camera frustum
- Calls: `CameraClass::Cull_Sphere`

### `W3DTreeBuffer::updateSway`
- Purpose: Updates tree sway based on breeze parameters
- Calls: `GameClientRandomValue`, `GameClientRandomValueReal`

### `W3DTreeBuffer::applyTopplingForce`
- Purpose: Initiates tree toppling with given force vector
- Calls: `FXList::doFXPos`

### `W3DTreeBuffer::updateTopplingTree`
- Purpose: Updates toppling physics (rotation, bouncing, sinking)
- Calls: `ThePartitionManager::getPropShroudStatusForPlayer`, `FXList::doFXPos`

### `W3DTreeBuffer::xfer`
- Purpose: Serializes tree data for network sync
- Calls: Xfer methods (`xferVersion`, `xferInt`, etc.)

## Globals
- `detailAlphaShader` (ShaderClass): Shader for alpha-blended tree rendering
- `detailAlphaShader2X` (ShaderClass): 2X shader variant
- `ANGULAR_LIMIT` (Real): Maximum rotation angle before bounce (PI/2 - PI/64)

## Dependencies
- Key includes: `W3DTreeBuffer.h`, `assetmgr.h`, `texture.h`, `WW3D2/DX8Wrapper.h`
- External symbols: `ThePlayerList`, `ThePartitionManager`, `TheTerrainRenderObject`, `TheWritableGlobalData`, `TheGlobalData`
