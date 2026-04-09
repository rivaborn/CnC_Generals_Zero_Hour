# Generals/Code/Libraries/Source/WWVegas/WW3D2/htree.h

## Purpose
Defines the HTreeClass, representing a hierarchy of coordinate systems (bones) for skeletal animation in the W3D engine.

## Responsibilities
- Manages bone hierarchy and transformations
- Handles animation updates (blending, interpolation)
- Provides bone capture/control for manual overrides
- Loads/saves W3D hierarchy data
- Supports morphing and interpolation between hierarchies

## Key Types
- HTreeClass (Class): Represents a bone hierarchy with initial transforms
- PivotClass (Class): Underlying pivot/bone data structure (forward declared)
- HAnimClass (Class): Animation data structure (forward declared)
- HAnimComboClass (Class): Animation combo structure (forward declared)
- HRawAnimClass (Class): Raw animation data structure (forward declared)
- (anonymous enum): Status codes (OK, LOAD_ERROR)

## Key Functions
### HTreeClass::Load_W3D
- Purpose: Loads hierarchy data from a W3D file chunk
- Calls: read_pivots

### HTreeClass::Blend_Update
- Purpose: Blends between two animations at specified frames
- Calls: Not inferable

### HTreeClass::Combo_Update
- Purpose: Updates hierarchy using an animation combo
- Calls: Not inferable

### HTreeClass::Simple_Evaluate_Pivot
- Purpose: Evaluates a single pivot's transform without full update
- Calls: Not inferable

### HTreeClass::Create_Morphed
- Purpose: Creates a morphed hierarchy from multiple source hierarchies
- Calls: Not inferable

### HTreeClass::Create_Interpolated
- Purpose: Creates an interpolated hierarchy between multiple sources
- Calls: Not inferable

## Globals
None

## Dependencies
- Key includes: "always.h", "pivot.h", "quat.h", "matrix3d.h", "vector3.h", "w3d_file.h", "wwdebug.h"
- External symbols: W3DMPO, ChunkLoadClass, ChunkSaveClass, Matrix3D, WWINLINE, WWASSERT
