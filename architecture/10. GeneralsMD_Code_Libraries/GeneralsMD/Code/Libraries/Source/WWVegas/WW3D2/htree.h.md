# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/htree.h

## Purpose
Defines the HTreeClass, representing a hierarchy of coordinate systems (bones) for skeletal animation in the W3D engine.

## Responsibilities
- Manages bone hierarchy and transformations
- Handles animation updates (blending, interpolation)
- Provides bone capture/control for manual overrides
- Loads/saves W3D hierarchy data
- Supports morphing and interpolation between hierarchies

## Key Types
- HTreeClass (Class): Represents a bone hierarchy with transforms and visibility
- (anonymous enum) (Enum): Defines status codes (OK, LOAD_ERROR)
- HAnimClass (Class): Forward declaration for animation data
- HAnimComboClass (Class): Forward declaration for animation combos
- MeshClass (Class): Forward declaration for mesh data
- ChunkLoadClass (Class): Forward declaration for loading chunks
- ChunkSaveClass (Class): Forward declaration for saving chunks
- HRawAnimClass (Class): Forward declaration for raw animation data

## Key Functions
### HTreeClass::Load_W3D
- Purpose: Loads hierarchy data from a W3D file chunk
- Calls: read_pivots

### HTreeClass::Anim_Update
- Purpose: Updates bone transforms based on animation data
- Calls: None visible

### HTreeClass::Blend_Update
- Purpose: Blends between two animations for smooth transitions
- Calls: None visible

### HTreeClass::Combo_Update
- Purpose: Updates hierarchy using animation combos
- Calls: None visible

### HTreeClass::Simple_Evaluate_Pivot
- Purpose: Evaluates a single pivot's transform without full update
- Calls: None visible

### HTreeClass::Scale
- Purpose: Scales the entire hierarchy by a factor
- Calls: None visible

### HTreeClass::Alter_Avatar_HTree
- Purpose: Morphs bones based on scale vector
- Calls: None visible

### HTreeClass::Create_Morphed
- Purpose: Creates a morphed hierarchy from multiple sources
- Calls: None visible

### HTreeClass::Create_Interpolated
- Purpose: Creates an interpolated hierarchy between sources
- Calls: None visible

## Globals
- None

## Dependencies
- Key includes: "always.h", "pivot.h", "quat.h", "matrix3d.h", "vector3.h", "w3d_file.h", "wwdebug.h"
- External symbols: W3DMPO, ChunkLoadClass, HAnimClass, HAnimComboClass, MeshClass, ChunkSaveClass, HRawAnimClass
