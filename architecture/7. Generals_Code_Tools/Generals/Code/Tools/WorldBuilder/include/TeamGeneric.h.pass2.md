# Generals/Code/Tools/WorldBuilder/include/TeamGeneric.h - Enhanced Analysis

## Architectural Role
This file defines the `TeamGeneric` class, a property page in WorldBuilder's MFC-based UI for configuring team properties. It bridges the gap between the editor's UI and the underlying `Dict` data structure, enabling modders to customize team behavior.

## Cross-References
### Incoming
- Likely called by WorldBuilder's property sheet manager when team properties need editing
- May be referenced by other property page classes for team-related configuration

### Outgoing
- Interacts with `Dict` for serialization/deserialization of team properties
- Uses MFC's `CPropertyPage` for dialog management
- Potentially calls into script system (e.g., for script list population)

## Design Patterns
- **Adapter Pattern**: Converts between `Dict` data and UI controls
- **Observer Pattern**: UI controls likely notify the class of changes via message handlers
- **Template Method**: `_scriptsToDict`/`_dictToScripts` suggest a two-way sync pattern

*Not inferable*: Exact script system integration or MFC message flow details.
