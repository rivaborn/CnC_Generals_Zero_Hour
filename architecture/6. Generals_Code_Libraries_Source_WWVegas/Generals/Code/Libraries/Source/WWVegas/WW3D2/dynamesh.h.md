# Generals/Code/Libraries/Source/WWVegas/WW3D2/dynamesh.h

## Purpose
Defines dynamic mesh rendering classes for the SAGE engine, supporting runtime geometry manipulation.

## Responsibilities
- Provides `DynamicMeshClass` for dynamic triangle rendering
- Implements `DynamicScreenMeshClass` for screen-space rendering
- Manages vertex attributes (position, normal, color, UV)
- Handles material/shader/texture assignment
- Supports triangle strips/fans and bounding volume queries

## Key Types
- **DynamicMeshModel (Class)**: Low-level mesh geometry with material properties
- **DynamicMeshClass (Class)**: High-level dynamic mesh render object
- **DynamicScreenMeshClass (Class)**: Screen-space variant of dynamic mesh
- **ShaderClass (Class)**: Reference to shader system (external)
- **IntersectionClass (Class)**: Reference to intersection system (external)
- **IntersectionResultClass (Class)**: Reference to intersection results (external)
- **MAX_COLOR_ARRAYS (Enum)**: Maximum color arrays constant
- **MAX_PASSES (Enum)**: Maximum render passes constant
- **TRI_MODE_STRIPS/TRI_MODE_FANS (Enum)**: Triangle rendering modes

## Key Functions
### DynamicMeshClass::Vertex
- Purpose: Shortcut for creating a vertex with position and UV
- Calls: `Begin_Vertex`, `Location`, `UV`, `End_Vertex`

### DynamicMeshClass::Switch_To_Multi_Vertex_Color
- Purpose: Initializes vertex color array with current color
- Calls: `Model->Get_Color_Array`, `DX8Wrapper::Convert_Color_Clamp`

### DynamicMeshClass::Set_Vertex_Color
- Purpose: Sets color for all vertices in a color array
- Calls: `Switch_To_Multi_Vertex_Color`

### DynamicScreenMeshClass::Location
- Purpose: Remaps coordinates to screen space
- Calls: None (inline coordinate transformation)

## Globals
- None

## Dependencies
- `meshgeometry.h`, `meshmatdesc.h`, `matinfo.h`, `rendobj.h`, `polyinfo.h`, `dx8wrapper.h`
- `Vector3`, `Vector4`, `Vector2`, `SphereClass`, `AABoxClass`, `TextureClass`, `VertexMaterialClass`
- `NEW_REF` macro for object creation
