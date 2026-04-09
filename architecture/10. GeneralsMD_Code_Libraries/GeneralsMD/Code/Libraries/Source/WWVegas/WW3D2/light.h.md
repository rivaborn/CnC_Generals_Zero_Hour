# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/light.h

## Purpose
Defines the LightClass, a render object representing a light source in the 3D engine.

## Responsibilities
- Manages light properties (type, intensity, color, attenuation)
- Handles spotlight-specific parameters (angle, direction, exponent)
- Provides scene graph integration (Notify_Added/Removed)
- Supports serialization via W3D chunk system

## Key Types
- **LightClass (Class)**: Represents a light source with various properties.
- **LightType (Enum)**: Defines light types (POINT, DIRECTIONAL, SPOT).
- **FlagsType (Enum)**: Controls light flags (NEAR_ATTENUATION, FAR_ATTENUATION).

## Key Functions
### `Notify_Added(SceneClass * scene)`
- Purpose: Registers light with the scene as a vertex processor.
- Calls: Not inferable.

### `Notify_Removed(SceneClass * scene)`
- Purpose: Unregisters light from the scene.
- Calls: Not inferable.

### `Get_Obj_Space_Bounding_Sphere(SphereClass & sphere)`
- Purpose: Calculates light's bounding sphere based on attenuation range.
- Calls: Not inferable.

### `Load_W3D(ChunkLoadClass & cload)`
- Purpose: Loads light data from W3D chunk.
- Calls: Not inferable.

### `Save_W3D(ChunkSaveClass & csave)`
- Purpose: Saves light data to W3D chunk.
- Calls: Not inferable.

## Globals
None.

## Dependencies
- `rendobj.h` (RenderObjClass)
- `w3derr.h` (WW3DErrorType)
- `always.h` (WWMath)
- ChunkLoadClass, ChunkSaveClass (forward
