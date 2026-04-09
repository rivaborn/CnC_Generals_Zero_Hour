# GeneralsMD/Code/GameEngine/Source/GameClient/Display.cpp

## Purpose
Manages the game's display system, including rendering views, handling video playback, and managing screen resolution.

## Responsibilities
- Manages display views (attachment, rendering, updating)
- Handles video playback (movies, logos, copyright screens)
- Controls screen resolution and windowed mode
- Provides debug display functionality

## Key Types
- **Display (Class)**: Main display manager singleton
- **View (Class)**: Base class for displayable views (referenced, not defined here)
- **DebugDisplayCallback (Type)**: Callback type for debug display (pointer to function)

## Key Functions
### `playLogoMovie`
- Purpose: Plays a logo movie with minimum display durations for movie and copyright.
- Calls: `stopMovie`, `TheVideoPlayer->open`, `createVideoBuffer`, `m_videoStream->width/height`

### `playMovie`
- Purpose: Plays a movie without additional hold times.
- Calls: `stopMovie`, `TheVideoPlayer->open`, `createVideoBuffer`

### `stopMovie`
- Purpose: Stops current movie playback and cleans up resources.
- Calls: `delete`, `m_videoStream->close`, `TheDisplayStringManager->freeDisplayString`

### `update`
- Purpose: Updates video playback state and handles frame rendering.
- Calls: `m_videoStream->isFrameReady/frameDecompress/frameRender/frameNext/frameIndex/frameCount`, `TheDisplayStringManager->newDisplayString`, `m_copyrightDisplayString->deleteInstance`, `TheGameText->fetch`, `TheFontLibrary->getFont`, `TheGlobalLanguageData->adjustFontSize`

### `setDisplayMode`
- Purpose: Changes screen resolution and adjusts tactical view proportions.
- Calls: `TheTacticalView->getWidth/getHeight/getOrigin/setWidth/setHeight/setOrigin`

## Globals
- **TheDisplay (Display*)**: Singleton instance of the Display class

## Dependencies
- Key includes: `Display.h`, `Mouse.h`, `VideoPlayer.h`, `DisplayStringManager.h`, `GameText.h`, `GlobalLanguage.h`
- External symbols: `TheMouse`, `TheTacticalView`, `TheVideoPlayer`, `TheDisplayStringManager`, `TheGameText`, `TheGlobalLanguageData`, `TheFontLibrary`
