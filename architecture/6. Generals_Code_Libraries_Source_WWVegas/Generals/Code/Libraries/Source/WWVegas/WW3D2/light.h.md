# Generals/Code/Libraries/Source/WWVegas/WW3D2/light.h

## Purpose
Defines the LightClass, a render object representing a light source in the 3D engine.

## Responsibilities
- Manages light properties (type, intensity, colors, attenuation)
- Handles spotlight-specific parameters (angle, direction, exponent)
- Provides scene graph integration (Notify_Added/Removed)
- Supports serialization via W3D chunk system
- Implements bounding volume queries

## Key Types
- **LightClass (Class)**: Represents a light source with various properties and behaviors.
- **LightType (Enum)**: Defines light types (POINT, DIRECTIONAL, SPOT).
- **FlagsType (Enum)**: Defines light flags (NEAR_ATTENUATION, FAR_ATTENUATION).

## Key Functions
### LightClass()
- Purpose: Constructs a LightClass with a specified type.
- Calls: Not inferable.

### Clone()
- Purpose: Creates a copy of the light.
- Calls: Not inferable.

### Notify_Added()
- Purpose: Registers the light with the scene as a vertex processor.
- Calls: Not inferable.

### Notify_Removed()
- Purpose: Unregisters the light from the scene.
- Calls: Not inferable.

### Get_Obj_Space_Bounding_Sphere()
- Purpose: Retrieves the light's bounding sphere.
- Calls: Not inferable.

### Get_Obj_Space_Bounding_Box()
- Purpose: Retrieves the light's bounding box.
- Calls: Not inferable.

### Load_W3D()
- Purpose: Loads light data from a W3D chunk.
- Calls: Not inferable.

### Save_W3D()
- Purpose: Saves light data to a W3D chunk.
- Calls: Not inferable.

## Globals
