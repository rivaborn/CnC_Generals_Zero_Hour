# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdlib.cpp

## Purpose
This file provides the library interface for WWShade, handling shader initialization, shutdown, and asset loader registration.

## Responsibilities
- Initialize and shutdown the shader renderer
- Manage shader initialization and cleanup
- Register asset loaders for shader-related assets
- Provide a flush mechanism for the shader system

## Key Types
None

## Key Functions
### SHD_Init
- Purpose: Initialize the shader renderer.
- Calls: ShdRendererClass::Peek_Instance()->Init()

### SHD_Shutdown
- Purpose: Shutdown the shader renderer.
- Calls: ShdRendererClass::Peek_Instance()->Shutdown()

### SHD_Init_Shaders
- Purpose: Initialize shaders.
- Calls: ShdRendererClass::Init_Shaders()

### SHD_Shutdown_Shaders
- Purpose: Shutdown shaders.
- Calls: ShdRendererClass::Shutdown_Shaders()

### SHD_Flush
- Purpose: Flush the shader system.
- Calls: ShdRendererClass::Peek_Instance()->Flush()

### SHD_Register_Loader
- Purpose: Register asset loaders for shader-related assets.
- Calls: WW3DAssetManager::Get_Instance()->Register_Prototype_Loader()

## Globals
None

## Dependencies
- shdlib.h
- assetmgr.h
- shdloader.h
- shdrenderer.h
- ShdRendererClass
- WW3DAssetManager
- _ShdMeshLoader
- _MeshLoader
