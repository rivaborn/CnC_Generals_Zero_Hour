# GeneralsMD/Code/GameEngineDevice/Include/VideoDevice/Bink/BinkVideoPlayer.h

## Purpose
Header defining Bink video playback classes for the SAGE engine.

## Responsibilities
- Declares `BinkVideoStream` and `BinkVideoPlayer` classes
- Defines interfaces for Bink video streaming and playback
- Manages Bink subsystem initialization and lifecycle

## Key Types
- **BinkVideoStream (Class)**: Bink video stream implementation
- **BinkVideoPlayer (Class)**: Bink video player implementation

## Key Functions
### BinkVideoStream::update
- Purpose: Update bink stream
- Calls: Not inferable

### BinkVideoStream::isFrameReady
- Purpose: Check if frame is ready for display
- Calls: Not inferable

### BinkVideoStream::frameRender
- Purpose: Render current frame to buffer
- Calls: Not inferable

### BinkVideoPlayer::init
- Purpose: Initialize video playback code
- Calls: Not inferable

### BinkVideoPlayer::open
- Purpose: Open video file for playback
- Calls: Not inferable

### BinkVideoPlayer::load
- Purpose: Load video file into memory for playback
- Calls: Not inferable

## Globals
- None

## Dependencies
- `VideoPlayer.h` (base class)
- `bink.h` (Bink SDK)
