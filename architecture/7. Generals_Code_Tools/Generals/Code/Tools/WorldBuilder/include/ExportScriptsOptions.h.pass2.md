# Generals/Code/Tools/WorldBuilder/include/ExportScriptsOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI configuration dialog for WorldBuilder's script export functionality, bridging the tool's UI layer with the script generation subsystem. It encapsulates user preferences for exporting different script types (units, waypoints, triggers) and provides accessors for these settings.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main UI framework when initiating script export operations
- Used by script generation modules that need to query export preferences

### Outgoing
- Relies on MFC dialog infrastructure (CDialog, CDataExchange)
- Interacts with WorldBuilder's script export implementation (not directly visible in header)

## Design Patterns
- **Property Accessor Pattern**: Getter methods expose export flags without revealing internal state
- **MVC (Model-View-Controller)**: Dialog acts as the view/controller for export configuration data
- **Static Member Pattern**: Uses static flags for shared export state across dialog instances

Rules followed. Output under 400 tokens.
