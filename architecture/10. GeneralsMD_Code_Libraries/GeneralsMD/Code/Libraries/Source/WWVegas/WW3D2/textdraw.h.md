# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/textdraw.h

## Purpose
Defines the `TextDrawClass` for rendering 2D text and primitives in a 3D scene using dynamic meshes.

## Responsibilities
- Manages dynamic mesh-based text and primitive rendering
- Handles coordinate transformations for screen rendering
- Provides text measurement and drawing utilities
- Supports basic 2D primitives (quads, lines)

## Key Types
- **Font3DInstanceClass (Class)**: External font rendering interface (not defined here)
- **TextDrawClass (Class)**: Main text/primitive rendering class inheriting from `DynamicMeshClass`

## Key Functions
### TextDrawClass()
- Purpose: Constructor initializing text draw with max character capacity
- Calls: Not inferable

### Print(Font3DInstanceClass*, char, float, float)
- Purpose: Renders a single character at screen coordinates
- Calls: Not inferable

### Print(Font3DInstanceClass*, const char*, float, float)
- Purpose: Renders a string at screen coordinates
- Calls: Not inferable

### Set_Coordinate_Ranges()
- Purpose: Configures coordinate transformation ranges
- Calls: Not inferable

### Quad()
- Purpose: Renders a textured quad primitive
- Calls: Not inferable

### Line()
- Purpose: Renders a line segment
- Calls: Not inferable

## Globals
- **CLASSID_TEXTDRAW (int)**: Class identifier constant

## Dependencies
- `DynamicMeshClass` (inheritance)
- `Font3DInstanceClass` (external)
- `Vector2`, `Vector3`, `RectClass` (math types)
- `VertexMaterialClass`, `ShaderClass` (rendering)
- `always.h`, `dynamesh.h`, `
