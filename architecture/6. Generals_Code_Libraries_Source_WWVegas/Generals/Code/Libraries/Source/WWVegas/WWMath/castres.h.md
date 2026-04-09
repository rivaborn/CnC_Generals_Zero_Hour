# Generals/Code/Libraries/Source/WWVegas/WWMath/castres.h

## Purpose
Defines a structure to store results of volume or ray cast operations in the SAGE engine.

## Responsibilities
- Holds collision detection results (fraction, normal, surface type)
- Supports optional contact point calculation
- Provides reset functionality for reuse
- Tracks initial interpenetration state

## Key Types
- **CastResultStruct (struct)**: Stores results of cast operations including collision fraction, normal, surface type, and optional contact point.

## Key Functions
### CastResultStruct::Reset
- Purpose: Resets all members to default values.
- Calls: None

## Globals
- None

## Dependencies
- `always.h`
- `vector3.h`
- `bittype.h`
- `W3D_SURFACE_TYPES` (referenced but not defined here)
