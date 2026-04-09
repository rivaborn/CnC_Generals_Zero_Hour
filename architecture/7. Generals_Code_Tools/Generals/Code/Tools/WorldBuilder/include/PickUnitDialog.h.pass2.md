# Generals/Code/Tools/WorldBuilder/include/PickUnitDialog.h - Enhanced Analysis

## Architectural Role
This header defines UI dialogs for unit selection/replacement in WorldBuilder, bridging the editor's data model (MapObject/ThingTemplate) with MFC-based UI controls. It encapsulates filtering logic for unit types/factions, exposing this functionality to other editor tools.

## Cross-References
### Incoming
- Editor tools (e.g., map placement/validation) likely instantiate `PickUnitDialog`/`ReplaceUnitDialog` for user input
- WorldBuilder's main frame may call `SetupAsPanel` to embed the dialog as a dockable panel

### Outgoing
- Uses `Common/AsciiString.h` and `Common/ThingSort.h` for string handling and unit categorization
- Interacts with MFC's `CTreeCtrl` for hierarchical display of units
- Relies on `MapObject` and `ThingTemplate` classes (defined elsewhere) for unit metadata

## Design Patterns
- **Composite**: Tree view structure groups units hierarchically (e.g., by faction/type)
- **Strategy**: Filtering via `SetAllowableType`/`IsAllowableType` allows dynamic behavior without subclassing
- **Template Method**: `OnInitDialog` sets up UI while derived classes (e.g., `ReplaceUnitDialog`) customize behavior

*Not inferable*: Exact relationship with W3D rendering system or networking layers.
