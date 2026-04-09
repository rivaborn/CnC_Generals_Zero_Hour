# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/metalmap.cpp

## Purpose
Manages dynamic metal/environment mapping textures for 3D rendering, updating them per-frame based on lighting conditions.

## Responsibilities
- Loads metal parameters from INI files
- Generates and updates metal map textures dynamically
- Handles lighting calculations (Phong/Blinn model)
- Manages texture resources and memory

## Key Types
- **MetalMapManagerClass**: Main class managing metal maps
- **MetalParams** (struct): Stores material properties (ambient/diffuse/specular colors, shininess)
- **Vector3**: Used for lighting calculations

## Key Functions
### `MetalMapManagerClass(INIClass &ini)`
- Purpose: Constructor that loads metal parameters from INI
- Calls: `initialize_normal_table()`, `initialize_metal_params()`

### `Update_Textures()`
- Purpose: Updates all metal map textures per frame based on current lighting
- Calls: `VectorProcessorClass::DotProduct()`, `VectorProcessorClass::ClampMin()`, `VectorProcessorClass::Power()`

### `initialize_normal_table()`
- Purpose: Creates a table of normalized vectors for lighting calculations
- Calls: None

## Globals
- **_NormalTable** (Vector3*): Static table of normalized vectors for lighting calculations

## Dependencies
- `metalmap.h`, `texture.h`, `ww3dformat.h`, `ww3d.h`, `vp.h`, `ini.h`, `point.h`, `stdio.h`, `hashtemplate.h`, `wwstring.h`, `wwmath.h`
- Uses `VectorProcessorClass`, `TextureClass`, `SurfaceClass`, `WW3D`
