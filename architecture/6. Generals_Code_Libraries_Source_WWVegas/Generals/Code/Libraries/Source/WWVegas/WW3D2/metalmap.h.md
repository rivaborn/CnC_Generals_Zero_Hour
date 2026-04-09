# Generals/Code/Libraries/Source/WWVegas/WW3D2/metalmap.h

## Purpose
Manages procedural environment maps (metal maps) for lighting effects using a Phong reflectance model.

## Responsibilities
- Manages metal map textures and their parameters
- Updates lighting and texture data per frame
- Provides access to metal maps by ID
- Initializes normal tables and metal parameters

## Key Types
- **MetalMapManagerClass (Class)**: Manages metal maps and lighting updates
- **MetalParams (Struct)**: Stores Phong reflectance parameters (ambient, diffuse, specular colors, shininess)
- **TextureClass (Class)**: Reference to texture data (external)
- **INIClass (Class)**: Reference to configuration data (external)

## Key Functions
### MetalMapManagerClass(INIClass &ini)
- Purpose: Constructor initializes metal map manager from INI file
- Calls: initialize_normal_table, initialize_metal_params

### Update_Lighting(const Vector3& ambient, const Vector3& main_light_color, const Vector3& main_light_dir, const Vector3& camera_dir)
- Purpose: Updates lighting parameters for metal map generation
- Calls: None

### Update_Textures(void)
- Purpose: Updates metal map textures once per frame before rendering
- Calls: None

### Get_Metal_Map(int id)
- Purpose: Retrieves a metal map texture by ID
- Calls: None

## Globals
- **_NormalTable (Vector3*)**: Static table of 16x16 camera-space normals for environment maps

## Dependencies
- `<vector3.h>` for Vector3 math
- `TextureClass` (external)
- `INIClass` (external)
