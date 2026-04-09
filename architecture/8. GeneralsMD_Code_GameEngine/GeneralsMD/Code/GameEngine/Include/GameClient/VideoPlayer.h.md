# GeneralsMD/Code/GameEngine/Include/GameClient/VideoPlayer.h

## Purpose
Defines interfaces and classes for video playback in the game engine, including video buffers, streams, and player management.

## Responsibilities
- Declares video playback interfaces (`VideoPlayerInterface`, `VideoStreamInterface`)
- Defines core classes for video handling (`VideoPlayer`, `VideoStream`, `VideoBuffer`)
- Manages video asset registration and retrieval
- Provides frame control and rendering capabilities

## Key Types
- **Video (struct)**: Stores video file metadata (filename, internal name, comment)
- **VideoBuffer (class)**: Abstract base class for video frame buffers with pixel format support
- **VideoStreamInterface (class)**: Interface for video stream operations (frame control, rendering)
- **VideoPlayerInterface (class)**: Interface for video playback management (stream handling, focus control)
- **VideoPlayer (class)**: Concrete implementation of video playback system
- **Type (enum)**: Pixel format types (R8G8B8, X8R8G8B8, R5G6B5, X1R5G5B5)

## Key Functions
### VideoPlayer::init
- Purpose: Initialize video playback system
- Calls: Not visible in header

### VideoPlayer::update
- Purpose: Service all video tasks (should be called frequently)
- Calls: Not visible in header

### VideoStream::frameRender
- Purpose: Render current frame into specified buffer
- Calls: Not visible in header

### VideoPlayer::open
- Purpose: Open video file for playback
- Calls: Not visible in header

## Globals
- **TheVideoPlayer (VideoPlayerInterface*)**: Global video player interface instance

## Dependencies
- `<lib/BaseType.h>`
- `WWMath/rect.h`
- `Common/SubsystemInterface.h`
- `Common/AsciiString.h`
- `Common/INI.h`
- `Common/STLTypedefs.h`
- `std::vector` for video management
