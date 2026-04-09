# GeneralsMD/Code/GameEngine/Include/GameClient/WindowVideoManager.h

## Purpose
Manages video playback in game windows, handling movie states and rendering.

## Responsibilities
- Tracks active video windows and their states
- Controls playback (play, pause, stop, hide)
- Manages video resources (buffers, streams)
- Handles bulk operations (stop/pause all movies)

## Key Types
- **WindowVideoPlayType (Enum)**: Movie playback modes (once, loop, show last frame)
- **WindowVideoStates (Enum)**: Video states (start, stop, pause, play, hidden)
- **WindowVideo (Class)**: Represents a single video playback instance
- **WindowVideoManager (Class)**: Manages collection of video playbacks
- **hashConstGameWindowPtr (Struct)**: Custom hash for GameWindow pointers

## Key Functions
### WindowVideoManager::playMovie
- Purpose: Start playing a movie in a window
- Calls: Not inferable

### WindowVideoManager::update
- Purpose: Update all active videos
- Calls: Not inferable

### WindowVideoManager::stopAllMovies
- Purpose: Stop all currently playing movies
- Calls: Not inferable

### WindowVideoManager::pauseAllMovies
- Purpose: Pause all currently playing movies
- Calls: Not inferable

## Globals
- **m_playingVideos (WindowVideoMap)**: Map of active video playbacks
- **m_stopAllMovies (Bool)**: Flag for global stop state
- **m_pauseAllMovies (Bool)**: Flag for global pause state

## Dependencies
- GameWindow, AsciiString, VideoStreamInterface, VideoBuffer (forward declarations)
- SubsystemInterface (inheritance)
- std::hash_map, std::hash, std::equal_to (STL containers)
