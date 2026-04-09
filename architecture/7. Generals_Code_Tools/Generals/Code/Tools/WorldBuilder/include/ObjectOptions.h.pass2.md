# Generals/Code/Tools/WorldBuilder/include/ObjectOptions.h - Enhanced Analysis

## Architectural Role
This header defines the `ObjectOptions` class, a key component of WorldBuilder's UI layer for object manipulation. It bridges the gap between the map editor's data model (`MapObject`) and the user interface, enabling object selection, property editing, and placement operations.

## Cross-References
### Incoming
- **WorldBuilder UI modules**: Likely called by the main WorldBuilder window and other dialogs that need to interact with object properties.
- **Map editing tools**: Used by terrain/heightmap editors (`WorldHeightMapEdit`) when objects need to be placed or modified.

### Outgoing
- **`ObjectPreview`**: For visual feedback during object selection.
- **`OptionsPanel`**: Base class for dialog behavior.
- **`MapObject`**: Core data structure for objects in the map.

## Design Patterns
- **Singleton-like access**: Uses `m_staticThis` for global access to the dialog instance, common in MFC-based tools.
- **Observer pattern**: The `update()` method suggests this class reacts to external state changes (e.g., object selection).
- **Composite pattern**: Tree view structure (`addObject`, `findOrAdd`) implies hierarchical organization of objects.

*Not inferable*: No clear use of Factory, Strategy, or Command patterns in the header.
