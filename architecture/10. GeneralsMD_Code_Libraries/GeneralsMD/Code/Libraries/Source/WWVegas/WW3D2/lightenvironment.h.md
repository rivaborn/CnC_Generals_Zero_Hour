# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/lightenvironment.h

## Purpose
Defines the `LightEnvironmentClass` for managing lighting calculations in the SAGE engine, handling both directional and point lights.

## Responsibilities
- Manages a collection of lights affecting an object
- Calculates lighting contributions (ambient, diffuse) for rendering
- Supports fill light for consistent lighting
- Provides accessors for light properties and LOD control

## Key Types
- **LightEnvironmentClass (Class)**: Main class for lighting environment management
- **InputLightStruct (Struct)**: Stores raw light data before transformation
- **OutputLightStruct (Struct)**: Stores transformed light data for rendering
- **Matrix3D (Class)**: Used for camera transformations (external)
- **LightClass (Class)**: Represents a light source (external)

## Key Functions
### `Reset`
- Purpose: Clears and initializes the light environment for a new object
- Calls: None visible

### `Add_Light`
- Purpose: Adds a light source to the environment
- Calls: `InputLightStruct::Init`

### `Pre_Render_Update`
- Purpose: Transforms lights into camera space before rendering
- Calls: `OutputLightStruct::Init`

### `Calculate_Fill_Light`
- Purpose: Computes a fill light to ensure consistent lighting
- Calls: None visible

### `operator==`
- Purpose: Compares two light environments for equality
- Calls: None visible

## Globals
- **MAX_LIGHTS (Enum)**: Maximum number of lights (4)

## Dependencies
- `vector3.h` (Vector3)
- `always.h`
- `Matrix3D` (forward declaration)
- `LightClass` (forward declaration)
