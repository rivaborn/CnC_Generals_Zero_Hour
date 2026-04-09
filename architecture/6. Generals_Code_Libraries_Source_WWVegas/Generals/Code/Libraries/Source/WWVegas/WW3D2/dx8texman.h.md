# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8texman.h

## Purpose
Header file defining texture management classes for DirectX 8 rendering in the SAGE engine.

## Responsibilities
- Declares `DX8TextureTrackerClass` for tracking texture properties
- Declares `DX8TextureManagerClass` for managing texture lifecycle
- Provides static methods for texture management operations
- Defines interfaces for texture addition/removal and resource management

## Key Types
- `DX8TextureTrackerClass` (Class): Tracks texture dimensions, format, mip levels, and render target status
- `DX8TextureManagerClass` (Class): Manages collection of textures and their lifecycle
- `DX8TextureTrackerList` (Type): Container for tracked textures (defined elsewhere)

## Key Functions
### `Shutdown`
- Purpose: Clean up texture manager resources
- Calls: Not inferable

### `Add`
- Purpose: Register a texture with the manager
- Calls: Not inferable

### `Remove`
- Purpose: Unregister a texture from the manager
- Calls: Not inferable

### `Release_Textures`
- Purpose: Release all managed textures
- Calls: Not inferable

### `Recreate_Textures`
- Purpose: Recreate all managed textures
- Calls: Not inferable

## Globals
- `Managed_Textures` (DX8TextureTrackerList): Static container storing all tracked textures

## Dependencies
- `always.h`, `texture.h`, `dx8wrapper.h`, `ww3dformat.h`, `dx8list.h`, `multilist.h`
- `TextureClass`, `MultiListObjectClass`, `WW3DFormat` types
- DirectX 8 texture management concepts
