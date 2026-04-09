# Generals/Code/Tools/WW3D/max2w3d/w3dexp.cpp

## Purpose
Handles W3D model export from 3DS Max, managing hierarchy, geometry, animation, and damage states.

## Responsibilities
- Export W3D model data (hierarchy, geometry, animation)
- Filter nodes for export (geometry, origins, damage roots)
- Validate export data (duplicate names, LOD extensions)
- Manage progress bars and user prompts
- Load/save hierarchy files

## Key Types
- **ExportInfoAppDataChunkStruct (Struct)**: Stores export options and padding for scene metadata
- **GeometryFilterClass (Class)**: Filters nodes for geometry export
- **OriginFilterClass (Class)**: Filters nodes for origin objects
- **DamageRootFilterClass (Class)**: Filters nodes for damage root objects
- **DamageRegionFilterClass (Class)**: Filters nodes for damage regions

## Key Functions
### DoExport
- Purpose: Main entry point for W3D export process
- Calls: get_export_options, DoOriginBasedExport, Export_Hierarchy, etc.

### DoOriginBasedExport
- Purpose: Handles new export path for multiple LODs/damage states
- Calls: get_damage_root_list, Start_Progress_Bar, Export_Hierarchy

### Export_HLod
- Purpose: Exports HLOD (Hierarchical LOD) descriptions
- Calls: HLodSaveClass::Save

### get_hierarchy_tree
- Purpose: Retrieves or loads hierarchy tree
- Calls: load_hierarchy_file

### get_damage_root_list
- Purpose: Creates list of damage root nodes
- Calls: None (uses DamageRootFilterClass)

## Globals
- **W3dExportClass::CurrentExportPath (char[])**: Stores current export directory path
- **houseColorScale (line 702)**: Not visible in provided context (likely in truncated section)

## Dependencies
- Key includes: rawfile.h, chunkio.h, w3dexp.h, nodelist.h, meshsave.h
- External symbols: INode, TimeValue, Matrix3, ExpInterface, Interface (3DS Max SDK)
- Helper classes: RawFileClass, ChunkSaveClass, HierarchySaveClass, HLodSaveClass
