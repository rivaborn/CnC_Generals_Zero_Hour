# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/CreditsMenu.cpp - Enhanced Analysis

## Architectural Role
This file implements the credits screen as a modal menu within the SAGE engine's UI system. It bridges the window management, audio, and credits management subsystems, handling lifecycle events (init/update/shutdown) and input routing for the credits sequence.

## Cross-References
### Incoming
- Called by the shell/window manager when the credits menu is pushed/popped (via `TheShell->pop()` and window callbacks)
- Input events routed from the window manager (keyboard focus and char messages)

### Outgoing
- Directly manipulates `TheCredits` (CreditsManager) for playback control
- Uses `TheWindowManager` for focus management and window lookup
- Controls audio via `TheAudio` (fading music, event triggers)
- Interacts with `TheShell` for menu stack management

## Design Patterns
- **Singleton Access**: Relies on global singletons (`TheCredits`, `TheAudio`, etc.) for subsystem access
- **Callback-Driven**: Implements a state machine via window message handlers (GWM_CREATE, GWM_INPUT_FOCUS, etc.)
- **Resource Management**: Explicit ownership of `TheCredits` with manual `new`/`delete` (no smart pointers)
