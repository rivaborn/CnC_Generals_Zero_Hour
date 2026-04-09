# Generals/Code/GameEngineDevice/Include/VideoDevice/Bink/BinkVideoPlayer.h

## Purpose
Header file defining Bink video playback classes for the SAGE engine.

## Responsibilities
- Declares `BinkVideoStream` and `BinkVideoPlayer` classes
- Defines interfaces for Bink video streaming and playback
- Manages Bink subsystem initialization and lifecycle

## Key Types
- **BinkVideoStream (Class)**: Handles individual video streams, frame management, and rendering
- **BinkVideoPlayer (Class)**: Manages video playback subsystem, stream creation, and system focus

## Key Functions
### `BinkVideoStream::update`
- Purpose: Updates the Bink stream
- Calls: Not inferable

### `BinkVideoPlayer::init`
- Purpose: Initializes video playback code
- Calls: Not inferable

### `BinkVideoPlayer::open`
- Purpose: Opens a video file for playback
- Calls: Not inferable

### `BinkVideoPlayer::load`
- Purpose: Loads a video file into memory for playback
- Calls: Not inferable

## Globals
- None

## Dependencies
- `VideoPlayer.h` (base class)
- `bink.h` (Bink SDK)
- `VideoStreamInterface` (abstract interface)
- `VideoBuffer` (rendering buffer)
- `AsciiString` (string type)
- `HBINK` (Bink handle type)
