# Generals/Code/Libraries/Source/WWVegas/WW3D2/lightenvironment.h

## Purpose
Manages lighting calculations for 3D objects by approximating local lighting from multiple light sources.

## Responsibilities
- Collects and processes point/directional lights affecting an object
- Calculates lighting contributions (ambient, diffuse) per light
- Transforms light directions into camera space for rendering
- Supports LOD-based lighting simplification

## Key Types
- **Matrix3D (Class)**: 3D transformation matrix (external)
- **LightClass (Class)**: Light source representation (external)
- **LightEnvironmentClass (Class)**: Main lighting environment manager
- **InputLightStruct (Struct)**: Stores raw light data before processing
- **OutputLightStruct (Struct)**: Stores processed light data for rendering
- **MAX_LIGHTS (Enum)**: Maximum supported lights (4)

## Key Functions
### LightEnvironmentClass::Reset
- Purpose: Clears lighting data and sets new object center/ambient
- Calls: None

### LightEnvironmentClass::Add_Light
- Purpose: Adds a light source to the environment
- Calls: InputLightStruct::Init

### LightEnvironmentClass::Pre_Render_Update
- Purpose: Transforms lights into camera space before rendering
- Calls: OutputLightStruct::Init

### LightEnvironmentClass::Set_Lighting_LOD_Cutoff
- Purpose: Sets threshold for converting weak lights to ambient
- Calls: None

### InputLightStruct::Contribution
- Purpose: Calculates light contribution based on distance/attenuation
- Calls: None

## Globals
- **LightingLODCutoff (static float)**: Threshold for LOD-based lighting simplification

## Dependencies
- `vector3.h` (Vector3)
- `always.h` (assertions)
- Matrix3D, LightClass
