# Generals/Code/GameEngine/Source/GameClient/GUI/WindowVideoManager.cpp

## Purpose
Manages video playback for game windows, handling movie creation, playback control, and resource cleanup.

## Responsibilities
- Tracks active video playback per window
- Manages video stream and buffer lifecycle
- Handles pause/stop/resume operations
- Updates video frames each frame
- Cleans up resources when windows are destroyed

## Key Types
- **WindowVideo (class)**: Represents a video playing in a specific window
- **WindowVideoManager (class)**: Manages all active video playbacks
- **WindowVideoStates (enum)**: Playback state (STOP, PLAY, PAUSE, HIDDEN)
- **WindowVideoPlayType (enum)**: Playback behavior (ONCE, LOOP, SHOW_LAST_FRAME)
- **WindowVideoMap (typedef)**: Map of GameWindow to WindowVideo

## Key Functions
### `WindowVideoManager::update`
- Purpose: Advances video frames and manages playback state transitions
- Calls: `isFrameReady`, `frameDecompress`, `frameRender`, `frameNext`, `stopMovie`, `pauseMovie`, `hideMovie`, `resumeMovie`

### `WindowVideoManager::playMovie`
- Purpose: Starts playback of a movie in a specified window
- Calls: `stopAndRemoveMovie`, `TheVideoPlayer->open`, `TheDisplay->createVideoBuffer`, `WindowVideo::init`

### `WindowVideoManager::stopAndRemoveMovie`
- Purpose: Stops and removes a movie from a window
- Calls: `WindowVideo::setWindowState`

## Globals
- **TheVideoPlayer (VideoPlayer)**: Global video player instance
- **TheDisplay (Display)**: Global display instance

## Dependencies
- `GameClient/WindowVideoManager.h`
- `GameClient/GameWindow.h`
- `GameClient/VideoPlayer.h`
- `GameClient/Display.h`
- `PreRTS.h`
