# Generals/Code/Tools/WW3D/max2w3d/meshsave.h

## Purpose
Header file defining the MeshSaveClass for exporting 3D meshes from 3ds Max to W3D format.

## Responsibilities
- Defines data structures for vertex and face data
- Declares MeshSaveClass for mesh export functionality
- Provides interface for writing mesh data to W3D files
- Handles material, texture, and shader export

## Key Types
- VertStruct (struct): Stores vertex data including position, normal, texture coords, and color
- FaceStruct (struct): Stores face data including vertex indices, material index, and face attributes
- MeshSaveClass (class): Main class for mesh export operations
- (anonymous enum): Exception error codes for mesh export

## Key Functions
### MeshSaveClass()
- Purpose: Constructor for MeshSaveClass
- Calls: Not inferable

### Write_To_File()
- Purpose: Writes mesh data to a W3D file
- Calls: write_header, write_user_text, write_verts, etc.

### Build_Mesh()
- Purpose: Processes mesh data using MeshBuilderClass
- Calls: Not inferable

### compute_bounding_volumes()
- Purpose: Computes bounding volumes for the mesh
- Calls: Not inferable

### write_verts()
- Purpose: Writes vertex data to the output file
- Calls: Not inferable

### write_triangles()
- Purpose: Writes triangle data to the output file
- Calls: Not inferable

### write_material_info()
- Purpose: Writes material information to the output file
- Calls: Not inferable

## Globals
- None

## Dependencies
- rawfile.h, Max.h, bittype.h, w3d_file.h, chunkio.h, progress.h, nodelist.h, util.h, w3dmtl.h, meshbuild.h, MeshDeformSave.H, w3dappdata.h
- HierarchySaveClass, MeshConnectionsClass, SkinDataClass (forward declarations)
