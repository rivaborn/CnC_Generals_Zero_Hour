# Generals/Code/Libraries/Source/WWVegas/WW3D2/bmp2d.h

## Purpose
Defines the `Bitmap2DObjClass` for rendering 2D bitmaps in the SAGE engine.

## Responsibilities
- Provides constructors for bitmap objects from files or textures
- Implements cloning and class identification
- Manages bitmap rendering properties (centering, additivity, colorization)

## Key Types
- **Bitmap2DObjClass (Class)**: Represents a 2D bitmap renderable object, inheriting from `DynamicScreenMeshClass`.

## Key Functions
### Bitmap2DObjClass (filename constructor)
- Purpose: Creates a bitmap from a file with specified rendering properties.
- Calls: `DynamicScreenMeshClass` constructor.

### Bitmap2DObjClass (texture constructor)
- Purpose: Creates a bitmap from an existing texture with specified rendering properties.
- Calls: `DynamicScreenMeshClass` constructor.

### Bitmap2DObjClass (copy constructor)
- Purpose: Copies a bitmap object.
- Calls: `DynamicScreenMeshClass` copy constructor.

### Clone
- Purpose: Creates a clone of the bitmap object.
- Calls: Not inferable.

### Class_ID
- Purpose: Returns the class identifier for the bitmap object.
- Calls: None.

## Globals
- None.

## Dependencies
- `dynamesh.h` (for `DynamicScreenMeshClass` base class)
- `RenderObjClass` (used in return type of `Clone`)
- `TextureClass` (used in constructor parameter)
- `CLASSID_BITMAP2D` (external constant)
