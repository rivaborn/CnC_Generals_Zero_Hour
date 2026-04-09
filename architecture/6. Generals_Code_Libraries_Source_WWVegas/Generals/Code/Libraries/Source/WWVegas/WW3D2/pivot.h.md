# Generals/Code/Libraries/Source/WWVegas/WW3D2/pivot.h

## Purpose
Defines the `PivotClass` structure representing nodes in a 3D hierarchy tree for the W3D engine.

## Responsibilities
- Stores transform data for hierarchy nodes
- Manages captured state for user-controlled pivots
- Provides visibility and indexing information
- Supports lazy allocation of capture matrices

## Key Types
- **PivotClass (struct)**: Represents a node in a 3D hierarchy with transform and capture state

## Key Functions
### PivotClass()
- Purpose: Default constructor
- Calls: None

### PivotClass(const PivotClass& that)
- Purpose: Copy constructor
- Calls: None

### operator=(const PivotClass& that)
- Purpose: Assignment operator
- Calls: None

### ~PivotClass()
- Purpose: Destructor that cleans up captured transform
- Calls: delete on CapTransformPtr (when LAZY_CAP_MTX_ALLOC is defined)

### Capture_Update()
- Purpose: Updates the captured transform state
- Calls: Not inferable

### Is_Captured()
- Purpose: Checks if the pivot is in captured state
- Calls: None

## Globals
- None

## Dependencies
- "always.h", "vector3.h", "matrix3d.h", "quat.h", "w3d_file.h"
- DynamicMatrix3D (used but not defined here)
- W3D_NAME_LEN (macro from w3d_file.h)
