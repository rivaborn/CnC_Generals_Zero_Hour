# GeneralsMD/Code/GameEngine/Source/GameClient/Eva.cpp - Enhanced Analysis

## Architectural Role
Eva.cpp implements the in-game AI assistant system, bridging game state monitoring (via Player/PlayerList) and audio playback (via TheAudio). It acts as a state-driven event dispatcher for player notifications, with priority-based scheduling and cooldown management.

## Cross-References
### Incoming
- GameLogic/GameLogic.h (likely calls playMessage/shouldPlay for state-triggered events)
- UI/IngameUI (may trigger EVA messages for UI-driven events)
- Networking (multiplayer sync for EVA state)

### Outgoing
- TheAudio (for sound event playback)
- Player/PlayerList (for state queries like energy levels)
- INI system (for configuration parsing)

## Design Patterns
- **Strategy Pattern**: `shouldPlayFuncs` array dispatches message-specific logic via function pointers.
- **Priority Queue**: `processPlayingMessages` selects highest-priority pending messages.
- **Observer-like**: Reacts to game state changes (e.g., low power) without direct coupling to sources.
