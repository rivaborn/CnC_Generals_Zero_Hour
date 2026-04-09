# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetPushButton.cpp - Enhanced Analysis

## Architectural Role
This file implements the core behavior for push button UI elements in the SAGE engine's GUI system. It bridges user input (mouse/keyboard) with visual feedback and audio cues, serving as a fundamental building block for all interactive UI components in the game.

## Cross-References
### Incoming
- **GameClient/GUI/Gadget/Gadget.cpp**: Likely registers this gadget type and dispatches messages to `GadgetPushButtonInput`/`GadgetPushButtonSystem`
- **GameClient/GUI/WindowManager/GameWindowManager.cpp**: Calls `GadgetButtonSetText` and other utility functions during window creation/updates
- **GameClient/InGameUI.cpp**: Uses push buttons for in-game menus (e.g., build queues, options)

### Outgoing
- **GameClient/GameWindowManager.h**: Relies heavily on `TheWindowManager` for message routing and window state management
- **Common/GameAudio.h**: Triggers audio events for button interactions via `TheAudio`
- **GameClient/Gadget.h**: Inherits from base `Gadget` class and uses its message system

## Design Patterns
- **Observer Pattern**: Buttons register as observers for mouse/keyboard events via `GadgetPushButtonInput`, reacting to system messages
- **State Pattern**: Explicit state management (hilited/selected) with bitmask flags (`WIN_STATE_HILITED`, `WIN_STATE_SELECTED`)
- **Decorator Pattern**: PushButtonData acts as a decorator for additional button-specific properties (borders, clocks) without modifying core `GameWindow` class

*Not inferable*: No clear use of Factory, Strategy, or Command patterns in the visible code.
