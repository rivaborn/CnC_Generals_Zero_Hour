# Generals/Code/Tools/WorldBuilder/include/WorldBuilder.h - Enhanced Analysis

## Architectural Role
This file serves as the central hub for the WorldBuilder tool's application layer, bridging MFC's document-view architecture with the game's map editing tools. It encapsulates tool management, clipboard operations, and application state, acting as a facade for the editing subsystem.

## Cross-References
### Incoming
- Tool implementations (BrushTool, TileTool, etc.) likely reference this for tool registration/activation
- View classes use `WbApp()` for global app access
- Document classes interact via `m_3dtemplate` for map data management

### Outgoing
- Directly uses MFC framework (CWinApp, CDocTemplate) for UI and document management
- Relies on Common utilities (STLTypedefs, Debug) for core types and assertions
- Tool subclasses inherit from base `Tool` class (not shown here)

## Design Patterns
- **Facade Pattern**: Exposes simplified interface (tool management) to complex MFC document-view system
- **Composite Pattern**: Manages collection of tools (m_tools array) as a single unit
- **Singleton Pattern**: Global `WbApp()` accessor provides single application instance

*Not inferable*: Exact inheritance hierarchy of tools or clipboard implementation details.
