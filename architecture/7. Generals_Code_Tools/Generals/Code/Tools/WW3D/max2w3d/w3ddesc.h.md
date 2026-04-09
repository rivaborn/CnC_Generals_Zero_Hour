# Generals/Code/Tools/WW3D/max2w3d/w3ddesc.h

## Purpose
Defines the class descriptor for the W3D exporter plugin in 3ds Max.

## Responsibilities
- Declares the `W3dClassDesc` class inheriting from `ClassDesc`
- Provides plugin metadata via overridden virtual methods
- Defines the plugin's unique class ID (`W3D_EXPORTER_CLASS_ID`)

## Key Types
- **W3dClassDesc (Class)**: Class descriptor for the W3D exporter plugin, providing metadata and factory methods.

## Key Functions
### W3dClassDesc::Create
- Purpose: Factory method to create an instance of the plugin.
- Calls: Not inferable (implementation not shown).

### W3dClassDesc::IsPublic
- Purpose: Indicates whether the plugin is publicly visible.
- Calls: Not inferable.

### W3dClassDesc::ClassName
- Purpose: Returns the human-readable name of the plugin class.
- Calls: Not inferable.

### W3dClassDesc::SuperClassID
- Purpose: Returns the superclass ID for the plugin.
- Calls: Not inferable.

### W3dClassDesc::ClassID
- Purpose: Returns the unique class ID of the plugin.
- Calls: Not inferable.

### W3dClassDesc::Category
- Purpose: Returns the category under which the plugin is listed.
- Calls: Not inferable.

## Globals
- **W3D_EXPORTER_CLASS_ID (Class_ID)**: Unique identifier for the W3D exporter plugin.

## Dependencies
- `always.h`: Likely contains common macros or definitions.
- `<Max.h>`: 3ds Max SDK header for `ClassDesc` and related types.
- Inherits from `ClassDesc` (3ds Max SDK).
