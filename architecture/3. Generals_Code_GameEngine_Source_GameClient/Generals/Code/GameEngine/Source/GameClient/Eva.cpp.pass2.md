# Generals/Code/GameEngine/Source/GameClient/Eva.cpp - Enhanced Analysis

## Architectural Role
This file implements the in-game voice announcement system (EVA), acting as a bridge between game state changes and audio playback. It manages event-driven announcements with priority-based scheduling, integrating tightly with the audio system and player state tracking.

## Cross-References
### Incoming
- **GameLogic**: Calls `Eva::playMessage()` when game events occur (e.g., low power, superweapon detection)
- **UI/Input**: Likely triggers announcements via player actions (e.g., "Building stolen" when a structure is captured)
- **Networking**: May receive remote EVA triggers in multiplayer (e.g., ally under attack notifications)

### Outgoing
- **Audio System**: Uses `TheAudio->addAudioEvent()` to play voice clips via `m_evaSpeech`
- **Player System**: Queries `ThePlayerList->getLocalPlayer()` for side-specific announcements
- **INI Parsing**: Relies on `INI::parse*` functions to load event configurations

## Design Patterns
- **Observer Pattern**: EVA system monitors game state changes (e.g., power levels) to trigger announcements
- **Priority Queue**: Uses `m_checks` vector with priority-based selection in `processPlayingMessages()`
- **Strategy Pattern**: `s_shouldPlayFuncs` array dispatches event-specific logic (e.g., `shouldPlayLowPower`)

*Not inferable*: Exact timing mechanism for `m_framesBetweenChecks` (likely tied to game loop FPS).
