# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/metalmap.h

## Purpose
Manages procedural environment maps (metal maps) for lighting effects using a Phong reflectance model.

## Responsibilities
- Manages metal map textures and parameters
- Updates lighting and textures per frame
- Provides access to metal maps by ID
- Initializes normal tables and metal parameters

## Key Types
- **MetalMapManagerClass (Class)**: Manages metal maps and lighting updates.
- **MetalParams (Struct)**: Stores Phong reflectance parameters (ambient, diffuse, specular colors, shininess).
- **TextureClass (Class)**: Reference to texture data (defined elsewhere).
- **INIClass (Class)**: Reference to INI configuration (defined elsewhere).

## Key Functions
### MetalMapManagerClass(INIClass &ini)
- Purpose: Constructs the manager and initializes metal maps from INI.
- Calls: `initialize_normal_table`, `initialize_metal_params`

### Update_Lighting(const Vector3& ambient, const Vector3& main_light_color, const Vector3& main_light_dir, const Vector3& camera_dir)
- Purpose: Updates lighting parameters for metal map generation.
- Calls: None

### Update_Textures(void)
- Purpose: Updates metal map textures before rendering.
- Calls: None

### Get_Metal_Map(int id)
- Purpose: Retrieves a metal map texture by ID.
- Calls: None

### Metal_Map_Count(void)
- Purpose: Returns the number of metal maps.
- Calls: None

## Globals
- **_NormalTable (Vector3*)**: Static table of camera-space normals for environment maps.

## Dependencies
- `<vector3.h>` for `Vector3`
- `TextureClass`, `INIClass` (forward-declared)
