# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8texman.cpp

## Purpose
Manages Direct3D 8 textures to handle device loss/reset scenarios.

## Responsibilities
- Tracks textures in a list
- Releases textures on device loss
- Recreates textures on device reset
- Adds/removes textures from management

## Key Types
- `DX8TextureManagerClass`: Manages texture lifecycle
- `TextureTrackerClass`: Tracks individual textures
- `TextureBaseClass`: Base texture class
- `TextureTrackerList`: Container for tracked textures

## Key Functions
### `Shutdown`
- Purpose: Cleans up all managed textures
- Calls: `Managed_Textures.Remove_Head()`, `delete`

### `Add`
- Purpose: Registers a texture for management
- Calls: `Managed_Textures.Add()`

### `Remove`
- Purpose: Unregisters a texture from management
- Calls: `it.Remove_Current_Object()`, `delete`

### `Release_Textures`
- Purpose: Releases all managed D3D textures
- Calls: `track->Release()`

### `Recreate_Textures`
- Purpose: Recreates lost textures after device reset
- Calls: `track->Recreate()`, `Get_Texture()->Set_Dirty()`

## Globals
- `Managed_Textures` (TextureTrackerList): Stores all tracked textures

## Dependencies
- `dx8texman.h`
- `TextureTrackerList`, `TextureTrackerListIterator` (list management)
- `TextureTrackerClass`, `TextureBaseClass` (texture abstractions)
