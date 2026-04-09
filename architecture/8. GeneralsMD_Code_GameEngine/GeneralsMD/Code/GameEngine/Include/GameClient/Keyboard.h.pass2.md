# GeneralsMD/Code/GameEngine/Include/GameClient/Keyboard.h - Enhanced Analysis

## Architectural Role
This file defines the core keyboard input subsystem, bridging low-level input handling with game logic. It abstracts platform-specific keyboard interactions while exposing a unified interface for modifier states, key translation, and event processing.

## Cross-References
### Incoming
- `GameClient/InputSystem.cpp` (likely calls `update()`, `getFirstKey()`, `setKeyStatusData`)
- `GameClient/UI/InputManager.cpp` (uses `isShift()`, `isCtrl()`, `isAlt()` for UI navigation)
- `GameClient/GameClient.cpp` (initializes `TheKeyboard` singleton)

### Outgoing
- **DirectX/Windows API**: `getKey()` implementation (pure virtual) delegates to platform-specific code
- `GameClient/KeyDefs.h`: Uses `KEY_STATE_*` constants for key state bitmasking
- `Common/SubsystemInterface.h`: Inherits from base subsystem class for engine integration

## Design Patterns
- **Singleton**: `TheKeyboard` global instance ensures single keyboard subsystem access
- **Template Method**: `update()` framework with `getKey()` hook for platform-specific behavior
- **State Pattern**: Key states tracked via bitmask (`m_keys[]`) with `getKeyStateBit()` accessor

*Not inferable*: Exact DirectX integration details or key repeat timing implementation.
