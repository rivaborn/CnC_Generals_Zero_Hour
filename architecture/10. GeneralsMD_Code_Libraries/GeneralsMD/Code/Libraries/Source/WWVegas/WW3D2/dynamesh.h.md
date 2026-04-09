# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dynamesh.h

## Purpose
Defines dynamic mesh rendering classes for the SAGE engine, supporting runtime geometry manipulation.

## Responsibilities
- Provides dynamic mesh model and render object classes
- Manages vertex, polygon, and material data for runtime geometry
- Supports triangle strips/fans and screen-space meshes
- Handles material, texture, and shader assignment
- Implements bounding volume calculations

## Key Types
- **DynamicMeshModel (Class)**: Low-level dynamic mesh geometry and material management
- **DynamicMeshClass (Class)**: High-level dynamic mesh render object with vertex/polygon manipulation
- **DynamicScreenMeshClass (Class)**: Screen-space variant of dynamic mesh
- **ShaderClass (Class)**: Reference to shader system (external)
- **IntersectionClass (Class)**: Reference to intersection system (external)
- **IntersectionResultClass (Class)**: Reference to intersection results (external)
- **MAX_COLOR_ARRAYS (Enum)**: Maximum color arrays constant
- **MAX_PASSES (Enum)**: Maximum render passes constant
- **TRI_MODE_STRIPS/TRI_MODE_FANS (Enum)**: Triangle rendering modes

## Key Functions
### DynamicMeshClass::Location
- Purpose: Sets vertex position in object space
- Calls: Model->Get_Vertex_Array()

### DynamicMeshClass::End_Vertex
- Purpose: Finalizes vertex creation and adds to triangle
- Calls: Flip_Face(), Model->Get_Polygon_Array()

### DynamicMeshClass::Switch_To_Multi_Vertex_Color
- Purpose: Converts mesh to use per-vertex colors
- Calls: Model->Get_Color_Array()

### DynamicMeshModel::Render
- Purpose: Renders the dynamic mesh with current state
- Calls: MatDesc rendering methods, Model->Get_*_Array() accessors

## Globals
- None

## Dependencies
- meshgeometry.h (MeshGeometryClass)
- meshmatdesc.h (MeshMatDescClass)
- matinfo.h (MaterialInfoClass)
- rendobj.h (RenderObjClass)
- polyinfo.h (PolygonInfoClass)
- dx8wrapper.h (DX8Wrapper)
- Vector3, Vector4, Vector2, AABoxClass, SphereClass, TriIndex
