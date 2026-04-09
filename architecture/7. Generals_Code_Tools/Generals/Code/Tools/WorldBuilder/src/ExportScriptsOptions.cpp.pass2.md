# Generals/Code/Tools/WorldBuilder/src/ExportScriptsOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements a configuration dialog for WorldBuilder's script export functionality, bridging the UI layer with the export system. It persists user preferences across sessions via static members, acting as a lightweight settings manager for the export pipeline.

## Cross-References
### Incoming
- Likely called from WorldBuilder's main menu or export workflow (e.g., via `CDialog`-derived invocation)
- Static members accessed by export logic (e.g., `ExportScriptsOptions::m_units`)

### Outgoing
- Uses MFC framework (`CDialog`, `CButton`) for UI rendering
- No direct calls to export logic inferred (pure UI layer)

## Design Patterns
- **Static Member Pattern**: Global-like state management for export preferences
- **MVC (Light)**: Separates UI (`CButton` controls) from state (`m_units`, etc.)
- **Template Method**: `OnInitDialog`/`OnOK` follow MFC's dialog lifecycle hooks

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns.
