# Generals/Code/Tools/WW3D/max2w3d/w3dexp.h

## Purpose
Defines the W3dExportClass for exporting 3D models from 3ds Max to W3D format.

## Responsibilities
- Implements SceneExport interface for W3D export
- Manages export options and progress tracking
- Handles hierarchy, animation, and geometry export
- Provides methods for damage animations and LOD export

## Key Types
- W3dExportClass (Class): Main export class handling W3D file generation
- MeshConnectionsClass (Class): Not defined here (forward declaration)
- GeometryExportTaskClass (Class): Not defined here (forward declaration)
- W3dExportOptionsStruct (Struct): Export configuration options

## Key Functions
### DoExport
- Purpose: Main export function that initiates the export process
- Calls: DoOriginBasedExport, get_export_options, get_origin_list, get_damage_root_list, get_hierarchy_tree, Export_Hierarchy, Export_Animation, Export_Damage_Animations, Export_Geometry, Export_HLod, Export_Collection

### DoOriginBasedExport
- Purpose: Handles origin-based export logic
- Calls: Not inferable

### Export_Hierarchy
- Purpose: Exports scene hierarchy to W3D format
- Calls: Not inferable

### Export_Animation
- Purpose: Exports animations to W3D format
- Calls: Not inferable

### Export_Damage_Animations
- Purpose: Exports damage-specific animations
- Calls: Not inferable

### Export_Geometry
- Purpose: Exports mesh geometry to W3D format
- Calls: Not inferable

### Export_HLod
- Purpose: Exports hierarchical LOD (Level of Detail) data
- Calls: Not inferable

### Export
