# GeneralsMD/Code/GameEngine/Source/GameClient/VideoPlayer.cpp

## Purpose
Manages video playback functionality in the game, including video stream handling and video resource management.

## Responsibilities
- Manages video streams and their lifecycle
- Provides interface for video playback control
- Handles video resource loading and unloading
- Maintains a registry of available videos
- Coordinates video rendering and updates

## Key Types
- **VideoPlayer (Class)**: Main video player interface managing streams and resources
- **VideoStream (Class)**: Base class for video stream implementation
- **VideoBuffer (Class)**: Handles video frame buffer management
- **Video (Struct)**: Represents video resource metadata
- **VideoPlayerInterface (Interface)**: Abstract interface for video player functionality

## Key Functions
### VideoPlayer::init
- Purpose: Initializes video player by loading configuration
- Calls: INI::load

### VideoPlayer::update
- Purpose: Updates all active video streams
- Calls: VideoStreamInterface::update

### VideoPlayer::open
- Purpose: Opens a video stream for playback
- Calls: None (returns NULL)

### VideoPlayer::addVideo
- Purpose: Adds a video to the available videos registry
- Calls: None

### VideoPlayer::removeVideo
- Purpose: Removes a video from the available videos registry
- Calls: None

### VideoStream::close
- Purpose: Closes and deletes the video stream
- Calls: VideoPlayer::remove

## Globals
- **TheVideoPlayer (VideoPlayerInterface*)**: Global instance of the video player

## Dependencies
- "PreRTS.h", "Lib/BaseType.h", "GameClient/VideoPlayer.h"
- INI class for configuration loading
- RectClass for rectangle operations
- AsciiString for string handling
- Vector and iterator templates for video registry
