# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8texman.h

## Purpose
Manages DirectX 8 texture resources, including creation, tracking, and recreation.

## Responsibilities
- Tracks texture objects and their properties
- Manages texture recreation after device loss
- Handles both regular and depth textures
- Provides global texture management interface

## Key Types
- **TextureTrackerClass (Class)**: Base class for tracking texture properties
- **DX8TextureTrackerClass (Class)**: Tracks standard textures with format/render target flags
- **DX8ZTextureTrackerClass (Class)**: Tracks depth textures with Z-format
- **DX8TextureManagerClass (Class)**: Global manager for texture resources

## Key Functions
### TextureTrackerClass::Recreate
- Purpose: Virtual method to recreate texture resources
- Calls: None (pure virtual)

### DX8TextureTrackerClass::Recreate
- Purpose: Recreates standard texture using DX8Wrapper
- Calls: DX8Wrapper::_Create_DX8_Texture

### DX8ZTextureTrackerClass::Recreate
- Purpose: Recreates depth texture using DX8Wrapper
- Calls: DX8Wrapper::_Create_DX8_ZTexture

### DX8TextureManagerClass::Recreate_Textures
- Purpose: Recreates all managed textures
- Calls: TextureTrackerClass::Recreate on all tracked textures

## Globals
- **Managed_Textures (TextureTrackerList)**: Static list of all tracked textures

## Dependencies
- "texture.h", "dx8wrapper.h", "ww3dformat.h", "dx8list.h", "multilist.h"
- TextureBaseClass, MultiListObjectClass, WW3DFormat, WW3DZFormat, MipCountType
- DX8Wrapper class methods for texture creation
