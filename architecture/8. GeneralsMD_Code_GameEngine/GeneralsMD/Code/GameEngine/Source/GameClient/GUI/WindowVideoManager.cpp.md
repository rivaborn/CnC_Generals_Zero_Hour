# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/WindowVideoManager.cpp

## Purpose
Manages video playback for game windows, handling movie creation, playback control, and resource cleanup.

## Responsibilities
- Tracks active video playback per window
- Manages video stream and buffer lifecycle
- Handles pause/stop/resume operations
- Updates video frames during gameplay
- Cleans up resources when windows are destroyed

## Key Types
- **WindowVideo (class)**: Represents a video playback instance for a specific window
- **WindowVideoManager (class)**: Central manager for all window video playback
- **WindowVideoStates (enum)**: Playback state (STOP, PLAY, PAUSE, HIDDEN)
- **WindowVideoPlayType (enum)**: Playback behavior (ONCE, LOOP, SHOW_LAST_FRAME)

## Key Functions
### `playMovie`
- Purpose: Starts playback of a movie in a specified window
- Calls: `TheVideoPlayer->open`, `TheDisplay->createVideoBuffer`, `WindowVideo::init`

### `update`
- Purpose: Advances video frames for all active playbacks
- Calls: `VideoStreamInterface::isFrameReady`, `frameDecompress`, `frameRender`, `frameNext`

### `stopAndRemoveMovie`
- Purpose: Stops and removes a video playback from a window
- Calls: `WindowVideo::setWindowState`, `m_playingVideos.erase`

## Globals
- **TheVideoPlayer (VideoPlayer)**: Global video player instance
- **TheDisplay (Display)**: Global display system reference

## Dependencies
- `GameClient/WindowVideoManager.h`
- `GameClient/GameWindow.h`
- `GameClient/VideoPlayer.h`
- `GameClient/Display.h`
- `PreRTS.h`
