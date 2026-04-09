# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8rendererdebugger.cpp

## Purpose
Provides debugging utilities for the DirectX 8 renderer, allowing inspection and manipulation of mesh objects.

## Responsibilities
- Tracks mesh objects with debug IDs
- Generates debug strings with mesh statistics
- Enables/disables meshes for rendering
- Manages mesh references and cleanup

## Key Types
- `MeshHash` (HashTemplateClass<unsigned, MeshClass*>): Stores mesh objects keyed by debug ID

## Key Functions
### `Enable(bool enable)`
- Purpose: Enables or disables the debugger
- Calls: None

### `Get_String(StringClass& s)`
- Purpose: Generates a debug string listing all tracked meshes with stats
- Calls: `MeshHash.Get()`, `MeshClass::Peek_Model()`, `MeshModelClass::Get_Polygon_Count()`, `MeshModelClass::Get_Vertex_Count()`, `MeshClass::Get_Name()`, `MeshClass::Is_Disabled_By_Debugger()`

### `Update()`
- Purpose: Releases all mesh references and clears the hash
- Calls: `MeshHash.Get()`, `MeshClass::Release_Ref()`, `MeshHash.Remove_All()`

### `Add_Mesh(MeshClass* mesh)`
- Purpose: Adds a mesh to the debugger's tracking (debug build only)
- Calls: `MeshHash.Get()`, `MeshClass::Get_Debug_Id()`, `MeshClass::Add_Ref()`, `MeshHash.Insert()`

### `Disable_Mesh(unsigned id)`
- Purpose: Disables rendering for a specific mesh by ID
- Calls: `MeshHash.Get()`, `MeshClass::Set_Debugger_Disable()`

### `Enable_Mesh(unsigned id)`
- Purpose: Enables rendering for a specific mesh by ID
- C
