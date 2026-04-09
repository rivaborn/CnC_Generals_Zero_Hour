# Generals/Code/Libraries/Source/WWVegas/WW3D2/lightenvironment.cpp

## Purpose
Manages lighting calculations for 3D objects, handling point, spot, and directional lights with LOD (Level of Detail) optimizations.

## Responsibilities
- Processes light sources into directional and ambient components
- Applies attenuation and spot light falloff calculations
- Manages light contribution sorting and LOD-based rejection
- Transforms lights into camera space for rendering
- Maintains ambient light accumulation

## Key Types
- `LightEnvironmentClass`: Main lighting manager
- `InputLightStruct`: Intermediate light representation before camera transform
- `OutputLightStruct`: Light data in camera space for rendering

## Key Functions
### `InputLightStruct::Init`
- Purpose: Initializes light data based on light type (point/spot/directional)
- Calls: `Init_From_Point_Or_Spot_Light`, `Init_From_Directional_Light`

### `Add_Light`
- Purpose: Adds a light source to the environment, handling LOD rejection
- Calls: `InputLightStruct::Init`, `Contribution`

### `Pre_Render_Update`
- Purpose: Transforms lights into camera space before rendering
- Calls: `OutputLightStruct::Init`

### `Set_Lighting_LOD_Cutoff`
- Purpose: Configures the LOD cutoff threshold for diffuse light rejection
- Calls: None

## Globals
- `DIFFUSE_TO_AMBIENT_FRACTION` (float): Fraction of diffuse light folded into ambient when rejected
- `_LightingLODCutoff` (float): Threshold for diffuse light LOD rejection
- `_LightingLODCutoff2` (float): Squared value of `_LightingLODCutoff` for optimization

## Dependencies
- `lightenvironment.h`, `matrix3d.h`, `camera.h`, `light.h`
- `Vector3`, `Matrix3D`, `LightClass`, `WWMath`
