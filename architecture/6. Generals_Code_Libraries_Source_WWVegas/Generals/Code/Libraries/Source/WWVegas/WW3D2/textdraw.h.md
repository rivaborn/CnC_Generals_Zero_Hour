# Generals/Code/Libraries/Source/WWVegas/WW3D2/textdraw.h

## Purpose
Defines the TextDrawClass for rendering 2D text and primitives in a 3D scene using dynamic meshes.

## Responsibilities
- Manage dynamic mesh-based text rendering
- Provide text measurement utilities
- Support primitive drawing (quads, lines)
- Handle coordinate transformations for screen rendering

## Key Types
- **Font3DInstanceClass (Class)**: External font rendering interface (not defined here)
- **TextDrawClass (Class)**: Main text rendering class extending DynamicMeshClass
- **Vector2 (Type)**: 2D vector for coordinates
- **Vector3 (Type)**: 3D vector for colors
- **RectClass (Type)**: Rectangle definition for UV mapping

## Key Functions
### TextDrawClass()
- Purpose: Constructor initializing text draw with max character capacity
- Calls: Not inferable

### Set_Coordinate_Ranges()
- Purpose: Configures coordinate transformation ranges
- Calls: Not inferable

### Print()
- Purpose: Renders text at specified screen coordinates
- Calls: Not inferable

### Quad()
- Purpose: Draws textured quad primitives
- Calls: Not inferable

### Line()
- Purpose: Draws line primitives
- Calls: Not inferable

## Globals
- **CLASSID_TEXTDRAW (const)**: Class identifier constant

## Dependencies
- DynamicMeshClass (inheritance)
- Font3DInstanceClass (usage)
- Vector2, Vector3, RectClass (types)
- VertexMaterialClass, ShaderClass (member types)
