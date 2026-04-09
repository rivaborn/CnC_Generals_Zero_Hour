# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/lightenvironment.cpp

## Purpose
Manages lighting calculations for 3D objects in the game, handling point, spot, and directional lights, and computing ambient/diffuse contributions.

## Responsibilities
- Processes light sources and computes their contributions to object lighting
- Manages a sorted list of active lights (up to MAX_LIGHTS)
- Calculates fill lighting to enhance primary light sources
- Handles LOD (Level of Detail) cutoff for lighting calculations
- Transforms lights into camera space for rendering

## Key Types
- **LightEnvironmentClass**: Main class managing lighting environment
- **InputLightStruct**: Stores pre-transformed light data (direction, ambient/diffuse, attenuation)
- **OutputLightStruct**: Stores camera-space light data for rendering

## Key Functions
### `LightEnvironmentClass::Add_Light`
- Purpose: Adds a light source to the environment, computing its contribution
- Calls: `InputLightStruct::Init`, `InputLightStruct::Contribution`

### `LightEnvironmentClass::Calculate_Fill_Light`
- Purpose: Computes a fill light from top 3 lights to enhance lighting
- Calls: `RGB_To_HSV`, `HSV_To_RGB`, `Add_Fill_Light`

### `LightEnvironmentClass::Pre_Render_Update`
- Purpose: Transforms lights into camera space before rendering
- Calls: `OutputLightStruct::Init`

## Globals
- **DIFFUSE_TO_AMBIENT_FRACTION (float)**: Fraction of diffuse light folded into ambient when below LOD cutoff
- **_LightingLODCutoff (float)**: Cutoff threshold for diffuse light rejection
- **_LightingLODCutoff2 (float)**: Squared value of _LightingLODCutoff

## Dependencies
- `lightenvironment.h`, `matrix3d.h`, `camera.h`, `light.h`, `colorspace.h`
- `LightClass`, `Vector3`, `Matrix3D`, `WWMath`
