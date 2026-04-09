# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwmouse.cpp - Enhanced Analysis

## Architectural Role
This file implements the core mouse input and cursor rendering system for the SAGE engine. It bridges OS-level mouse events with the game's logical coordinate system and handles cursor visibility management during rendering cycles.

## Cross-References
### Incoming
- UI systems (e.g., menu navigation, button hover effects)
- Input handling subsystems (e.g., command selection, unit targeting)
- Rendering pipeline (cursor drawing during frame composition)

### Outgoing
- Windows API (mouse position/query functions)
- Surface/Blit subsystems (cursor rendering/background restoration)
- ShapeSet system (cursor image management)

## Design Patterns
- **Singleton-like access** via `_MousePtr` global for cross-module mouse state queries
- **Double buffering** for cursor rendering (background save/restore)
- **Event-driven processing** via Windows timer callback for position updates

*Not inferable: Exact observer relationships with UI/input systems.*
