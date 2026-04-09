# Generals/Code/Tools/WW3D/max2w3d/geometryexportcontext.h

## Purpose
Defines the `GeometryExportContextClass` used during geometry export in the Max2W3D tool.

## Responsibilities
- Encapsulates data structures needed for geometry export
- Manages export context state (model name, transforms, options)
- Provides access to export-related classes (chunk saver, world info, hierarchy)
- Tracks material colors and progress meter

## Key Types
- **GeometryExportContextClass (Class)**: Main export context container
- **ChunkSaveClass (Class)**: Reference to chunk saving utility
- **MaxWorldInfoClass (Class)**: Reference to world information
- **HierarchySaveClass (Class)**: Reference to hierarchy saving utility
- **INodeListClass (Class)**: Reference to node list utility
- **Progress_Meter_Class (Class)**: Reference to progress meter
- **W3dExportOptionsStruct (Struct)**: Export configuration options

## Key Functions
### GeometryExportContextClass()
- Purpose: Constructs export context with model name, references, and initial state
- Calls: `strdup()`, `GetNodeTM()`

### ~GeometryExportContextClass()
- Purpose: Cleans up allocated resources (model name)
- Calls: `delete[]`

## Globals
- None

## Dependencies
- `<Max.h>` (3ds Max SDK)
- Forward declarations: `ChunkSaveClass`, `MaxWorldInfoClass`, `HierarchySaveClass`, `INodeListClass`, `Progress_Meter_Class`, `W3dExportOptionsStruct`
- External types: `INode`, `Matrix3`, `TimeValue` (from 3ds Max SDK)
