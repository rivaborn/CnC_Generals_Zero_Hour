# Generals/Code/Libraries/Source/WWVegas/WW3D2/metalmap.cpp

## Purpose
Manages dynamic metal map textures for rendering metallic surfaces with lighting effects.

## Responsibilities
- Loads metal parameters from INI files
- Generates and updates metal map textures per frame
- Handles lighting calculations (Phong/Blinn model)
- Manages normal map table for lighting calculations

## Key Types
- `MetalMapManagerClass`: Manages metal map generation and updates
- `MetalParams` (struct): Stores ambient/diffuse/specular colors and shininess per metal type
- `Vector3`: Used for lighting calculations

## Key Functions
### `MetalMapManagerClass(INIClass &ini)`
- Purpose: Constructs manager from INI configuration
- Calls: `initialize_normal_table`, `initialize_metal_params`

### `Update_Textures()`
- Purpose: Updates all metal map textures with current lighting
- Calls: `VectorProcessorClass::DotProduct`, `VectorProcessorClass::ClampMin`, `VectorProcessorClass::Power`

### `initialize_normal_table()`
- Purpose: Creates precomputed normal vectors for lighting calculations
- Calls: None

## Globals
- `_NormalTable` (Vector3*): Static table of precomputed normals

## Dependencies
- `metalmap.h`, `texture.h`, `ww3dformat.h`, `vp.h`, `ini.h`, `point.h`, `stdio.h`, `hashtemplate.h`, `wwstring.h`
- `VectorProcessorClass`, `SurfaceClass`, `TextureClass`
