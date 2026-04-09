# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/pivot.h

## Purpose
Defines the `PivotClass` structure representing nodes in a 3D hierarchy tree for the W3D engine.

## Responsibilities
- Stores transform data for hierarchy nodes
- Manages captured state for user-controlled pivots
- Provides visibility and world-space translation flags
- Supports lazy allocation of capture transforms

## Key Types
- **PivotClass (struct)**: Represents a node in a 3D hierarchy with transform and capture state

## Key Functions
### PivotClass()
- Purpose: Default constructor
- Calls: Not inferable

### PivotClass(const PivotClass& that)
- Purpose: Copy constructor
- Calls: Not inferable

### operator=(const PivotClass& that)
- Purpose: Assignment operator
- Calls: Not inferable

### ~PivotClass()
- Purpose: Destructor that cleans up lazy-allocated capture transforms
- Calls: `delete` (conditional on `LAZY_CAP_MTX_ALLOC`)

### Capture_Update()
- Purpose: Updates the captured transform state
- Calls: Not inferable

### Is_Captured()
- Purpose: Checks if the pivot is in captured state
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `vector3.h`, `matrix3d.h`, `quat.h`, `w3d_file.h`
- `DynamicMatrix3D` (used conditionally)
- `W3D_NAME_LEN` constant
