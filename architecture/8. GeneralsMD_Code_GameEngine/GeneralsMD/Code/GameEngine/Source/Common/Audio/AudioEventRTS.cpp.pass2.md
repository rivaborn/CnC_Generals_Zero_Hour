# GeneralsMD/Code/GameEngine/Source/Common/Audio/AudioEventRTS.cpp - Enhanced Analysis

## Architectural Role
This file implements the core audio event system, bridging game logic (objects/drawables) with the audio subsystem. It handles spatial audio positioning, event prioritization, and asset localization, serving as the primary interface for triggering in-game sounds.

## Cross-References
### Incoming
- **Game Logic**: Calls `findObjectByID` to resolve object positions
- **Game Client**: Calls `findDrawableByID` for drawable positions
- **Audio System**: Uses `TheAudio` for settings and playback
- **File System**: Checks for localized audio files

### Outgoing
- **Audio Subsystem**: Sets up playback parameters via `generatePlayInfo`
- **Game Logic**: Queries object states for positional audio
- **File System**: Validates asset existence for localization

## Design Patterns
- **State Pattern**: `OwnerType` enum and `getCurrentPosition` logic manage different audio source states (object, drawable, positional)
- **Strategy Pattern**: `generateFilenamePrefix/Extension` abstract filename construction based on audio type
- **Singleton Access**: Uses global `TheAudio`, `TheGameLogic`, etc. for subsystem coordination

*Not inferable*: Exact event queueing mechanism or priority handling details.
