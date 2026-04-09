# Generals/Code/GameEngine/Source/GameClient/VideoPlayer.cpp

## Purpose
Manages video playback functionality in the game client, including video stream handling and video buffer management.

## Responsibilities
- Manages video streams and buffers
- Provides interface for video playback control
- Handles video stream lifecycle (open/close/update)
- Maintains a registry of available videos
- Supports video buffer texture coordinate calculations

## Key Types
- **VideoPlayer (Class)**: Main video player interface implementation
- **VideoStream (Class)**: Base class for video stream handling
- **VideoBuffer (Class)**: Manages video frame buffers and texture coordinates
- **Video (Struct)**: Contains video metadata (filename, comments)
- **VideoPlayerInterface (Interface)**: Abstract video player interface

## Key Functions
### VideoPlayer::init
- Purpose: Initializes video player by loading video configuration
- Calls: INI::load

### VideoPlayer::update
- Purpose: Updates all active video streams
- Calls: VideoStreamInterface::update

### VideoPlayer::closeAllStreams
- Purpose: Closes all active video streams
- Calls: VideoStreamInterface::close

### VideoBuffer::Rect
- Purpose: Calculates texture coordinates for a video buffer rectangle
- Calls: None

### VideoStream::close
- Purpose: Closes the video stream and deletes itself
- Calls: VideoPlayer::remove

## Globals
- **TheVideoPlayer (VideoPlayerInterface*)**: Global video player instance

## Dependencies
- "GameClient/VideoPlayer.h" (header)
- "Lib/BaseType.h"
- "PreRTS.h"
- INI class for configuration loading
- AsciiString for string handling
- RectClass for rectangle operations
