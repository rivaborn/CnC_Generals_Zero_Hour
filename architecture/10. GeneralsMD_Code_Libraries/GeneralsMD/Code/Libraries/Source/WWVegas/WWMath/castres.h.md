# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/castres.h

## Purpose
Defines a structure to store results of volume or ray cast operations in the SAGE engine.

## Responsibilities
- Stores collision detection results (fraction, normal, surface type)
- Provides contact point calculation option
- Tracks initial interpenetration state
- Resets to default values

## Key Types
- **CastResultStruct (struct)**: Holds results of cast operations (collision fraction, normal, surface type, contact point)

## Key Functions
### CastResultStruct::Reset
- Purpose: Resets all members to default values
- Calls: None

## Globals
- None

## Dependencies
- `always.h`
- `vector3.h`
- `bittype.h`
- `W3D_SURFACE_TYPES` (referenced but not defined here)
