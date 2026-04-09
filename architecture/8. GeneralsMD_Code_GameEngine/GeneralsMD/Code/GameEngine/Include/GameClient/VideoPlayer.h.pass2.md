# GeneralsMD/Code/GameEngine/Include/GameClient/VideoPlayer.h - Enhanced Analysis

## Architectural Role
This header defines the core video playback subsystem in the SAGE engine, bridging between the game's rendering pipeline and media assets. It provides abstract interfaces for video buffering, streaming, and playback control, enabling both in-game cutscenes and UI animations.

## Cross-References
### Incoming
- Likely called by UI systems (e.g., `GameClient/UI.h`) for cutscene playback
- Used by mission/level loading systems for intro/outro videos
- Referenced by audio subsystem for synchronized video/audio playback

### Outgoing
- Depends on `SubsystemInterface` for engine integration
- Uses `WWMath/rect.h` for rendering coordinates
- Interfaces with platform-specific video decoding backends

## Design Patterns
- **Interface Segregation**: `VideoPlayerInterface` and `VideoStreamInterface` separate concerns
- **Factory Method**: `VideoPlayer::open()`/`load()` abstract video initialization
- **Observer**: `notifyVideoPlayerOfNewProvider()` suggests audio/video synchronization hooks

*Not inferable*: Concrete video decoding implementation details.
