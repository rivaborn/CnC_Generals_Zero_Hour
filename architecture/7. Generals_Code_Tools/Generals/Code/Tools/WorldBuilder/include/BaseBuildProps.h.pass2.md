# Generals/Code/Tools/WorldBuilder/include/BaseBuildProps.h - Enhanced Analysis

## Architectural Role
This header defines the UI dialog for the WorldBuilder tool's building property editor, bridging the MFC-based UI layer with the game's data model. It encapsulates the property management for buildings, serving as a critical component in the level editing workflow.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main editor UI (e.g., when "Edit Building" is selected)
- May be referenced by other property dialog classes (e.g., for inheritance)

### Outgoing
- Uses MFC's `CDialog` and `CDataExchange` for UI handling
- Relies on custom types (`AsciiString`, `Int`, `Bool`) from the engine's core utilities

## Design Patterns
- **MVC (Model-View-Controller)**: Separates building properties (model) from UI controls (view) and event handling (controller)
- **Data Transfer Object**: Encapsulates building properties for transfer between UI and backend
- **Template Method**: Overrides MFC virtual methods (`DoDataExchange`, `OnInitDialog`) to customize behavior

*Not inferable*: No clear use of Factory, Observer, or other patterns without seeing implementation.
