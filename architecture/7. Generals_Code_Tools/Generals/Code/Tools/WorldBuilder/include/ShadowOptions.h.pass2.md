# Generals/Code/Tools/WorldBuilder/include/ShadowOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for shadow configuration in WorldBuilder, bridging MFC dialog handling with the engine's rendering pipeline. It encapsulates user-facing controls for adjusting shadow properties that likely propagate to the W3D renderer.

## Cross-References
### Incoming
- WorldBuilder's main dialog framework (likely calls `ShadowOptions` constructor)
- Resource compiler (links to `IDD_SHADOW_OPTIONS` dialog template)

### Outgoing
- MFC framework (`CDialog`, `CDataExchange`)
- W3D renderer (via `setShadowColor`âimplied by `Real` type usage)
- WorldBuilder's project settings system (stores/loads shadow config)

## Design Patterns
- **MVC (Model-View-Controller)**: Dialog acts as View/Controller, with shadow properties as Model
- **Observer**: Event handlers (`OnChange*`) react to UI changes (Push model)
- **Template Method**: `DoDataExchange` as a hook for MFC's DDX/DDV mechanism

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
