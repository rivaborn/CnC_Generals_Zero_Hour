# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetTabControl.h - Enhanced Analysis

## Architectural Role
This header defines the UI tab control abstraction layer, bridging the generic GameWindow system with tab-specific functionality. It encapsulates tab management logic while delegating rendering to the underlying GameWindow implementation.

## Cross-References
### Incoming
- UI-related files (e.g., dialogs, menus) that need tabbed interfaces
- GameWindow subclasses that implement tab controls

### Outgoing
- Directly calls into GameWindow methods (winSetEnabledImage, etc.)
- Likely used by UI initialization code during game startup

## Design Patterns
- **Facade Pattern**: Provides simplified interface to complex GameWindow tab functionality
- **Inline Wrapper Pattern**: Uses inline functions to avoid runtime overhead while maintaining clean API
- **State Pattern**: Manages different visual states (enabled/disabled/hilite) for tabs

*Not inferable*: Exact implementation details of tab region computation or sub-pane management.
