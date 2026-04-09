# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bmp2d.h

## Purpose
Defines the `Bitmap2DObjClass` for rendering 2D bitmaps in the SAGE engine.

## Responsibilities
- Provides constructors for bitmap objects from files or textures
- Implements cloning and class identification
- Inherits from `DynamicScreenMeshClass` for rendering

## Key Types
- **Bitmap2DObjClass (Class)**: 2D bitmap rendering object with texture and display options

## Key Functions
### Bitmap2DObjClass (filename constructor)
- Purpose: Creates a bitmap from a file with specified dimensions and rendering flags
- Calls: `DynamicScreenMeshClass` constructor

### Bitmap2DObjClass (texture constructor)
- Purpose: Creates a bitmap from an existing texture with rendering flags
- Calls: `DynamicScreenMeshClass` constructor

### Bitmap2DObjClass (copy constructor)
- Purpose: Copies a bitmap object
- Calls: `DynamicScreenMeshClass` copy constructor

### Clone
- Purpose: Creates a deep copy of the bitmap object
- Calls: Not inferable

### Class_ID
- Purpose: Returns the class identifier for type checking
- Calls: None

## Globals
- None

## Dependencies
- `dynamesh.h` (for `DynamicScreenMeshClass` base)
- `CLASSID_BITMAP2D` (external constant)
