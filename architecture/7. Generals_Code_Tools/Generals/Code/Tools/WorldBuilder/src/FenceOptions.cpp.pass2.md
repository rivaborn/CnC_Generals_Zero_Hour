# Generals/Code/Tools/WorldBuilder/src/FenceOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the fence object selection UI in WorldBuilder, acting as a specialized front-end for the generic ObjectOptions panel. It bridges the editor's object placement system with fence-specific configuration (spacing/offset) while delegating actual object creation to the underlying ObjectOptions subsystem.

## Cross-References
### Incoming
- **ObjectOptions.h**: Calls `ObjectOptions::selectObject()` and queries `ObjectOptions::getCurGdfName()`
- **ThingFactory.h**: Iterates templates via `TheThingFactory->firstTemplate()`
- **ThingTemplate.h**: Accesses template properties (`getFenceWidth()`, `getFenceXOffset()`, etc.)
- **WorldBuilderDoc.h**: (Commented-out reference suggests historical coupling)

### Outgoing
- **MFC UI Framework**: Uses `CWnd`, `CDialog`, `CString` for dialog management
- **Tree View Controls**: Manages `CTreeView` for object hierarchy display
- **Common Types**: Uses `MapObject` (linked list) for internal object storage

## Design Patterns
- **Facade Pattern**: Presents a simplified fence-specific interface over the generic ObjectOptions system
- **Observer Pattern**: Reacts to tree view notifications (selection changes) via `OnNotify`
- **Singleton-like**: Uses `m_staticThis` for global access (though not a pure singleton)

*Not inferable*: No clear use of Strategy, Factory, or Command patterns despite the object creation context.
