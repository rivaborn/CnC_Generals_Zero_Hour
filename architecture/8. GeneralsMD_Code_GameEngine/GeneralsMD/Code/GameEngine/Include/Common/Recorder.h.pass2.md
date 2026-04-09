# GeneralsMD/Code/GameEngine/Include/Common/Recorder.h - Enhanced Analysis

## Architectural Role
This file defines the core replay system, bridging the game's networking layer (GameInfo) and message streaming (MessageStream). It handles serialization/deserialization of game state for replays, with special attention to multiplayer integrity via CRC validation.

## Cross-References
### Incoming
- **GameEngine**: Likely called by the main game loop for updates (update/playback/record)
- **Networking**: Uses GameInfo for slot management during playback
- **UI**: initControls() suggests UI subsystem integration for replay controls

### Outgoing
- **MessageStream**: Uses MessageStream for serializing/deserializing GameMessages
- **File I/O**: Directly interacts with FILE* for replay file operations
- **CRC Validation**: Integrates with CRCInfo for replay integrity checks

## Design Patterns
- **Singleton**: TheRecorder global instance ensures single replay system access
- **Strategy**: RecorderModeType switches behavior between record/playback/none states
- **Adapter**: ReplayGameInfo extends GameInfo to adapt slot data for replays

*Not inferable*: Exact CRCInfo implementation or MessageStream details.
