# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8texman.cpp

## Purpose
Manages Direct3D 8 textures in the default pool, ensuring proper release on device loss and recreation on device reset.

## Responsibilities
- Tracks textures via `DX8TextureTrackerClass` objects
- Releases internal D3D texture references
- Recreates textures after device reset
- Provides shutdown cleanup

## Key Types
- `DX8TextureManagerClass`: Manages texture lifecycle
- `DX8TextureTrackerClass`: Tracks individual texture state
- `DX8TextureTrackerList`: Container for managed textures

## Key Functions
### `Shutdown`
- Purpose: Cleans up all managed texture trackers
- Calls: `Managed_Textures.Remove_Head()`, `delete`

### `Add`
- Purpose: Registers a texture for management
- Calls: `Managed_Textures.Add()`

### `Remove`
- Purpose: Unregisters a texture from management
- Calls: `Managed_Textures` iterator methods, `delete`

### `Release_Textures`
- Purpose: Releases all D3D texture references
- Calls: `D3DTexture->Release()`, iterator methods

### `Recreate_Textures`
- Purpose: Recreates lost textures after device reset
- Calls: `DX8Wrapper::_Create_DX8_Texture()`, iterator methods

## Globals
- `Managed_Textures` (`DX8TextureTrackerList`): Stores all tracked textures

## Dependencies
- `dx8texman.h`
- `DX8TextureTrackerClass`
- `TextureClass`
- `DX8Wrapper` (external)
- `D3DTexture` (Direct3D 8)
