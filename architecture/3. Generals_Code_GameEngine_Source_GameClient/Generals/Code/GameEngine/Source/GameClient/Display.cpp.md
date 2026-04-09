# Generals/Code/GameEngine/Source/GameClient/Display.cpp

## Purpose
Manages the game's display system, including rendering views, handling movies, and managing screen resolution.

## Responsibilities
- Manages display views (attachment, rendering, updating)
- Handles movie playback (logo movies, regular movies)
- Manages screen resolution and mode changes
- Provides debug display functionality

## Key Types
- Display (Class): Main display manager singleton
- DebugDisplayCallback (Type): Callback type for debug display

## Key Functions
### Display::deleteViews
- Purpose: Deletes all views attached to the display
- Calls: View::getNextView, delete

### Display::attachView
- Purpose: Attaches a view to the display
- Calls: View::prependViewToList

### Display::drawViews
- Purpose: Renders all views attached to the display
- Calls: View::drawView

### Display::updateViews
- Purpose: Updates all views without rendering
- Calls: View::updateView

### Display::playLogoMovie
- Purpose: Plays a logo movie with minimum display durations
- Calls: stopMovie, TheVideoPlayer::open, createVideoBuffer

### Display::playMovie
- Purpose: Plays a regular movie
- Calls: stopMovie, TheVideoPlayer::open, createVideoBuffer

### Display::stopMovie
- Purpose: Stops the currently playing movie
- Calls: delete, TheVideoPlayer::close, TheDisplayStringManager::freeDisplayString

### Display::update
- Purpose: Updates the display state (movie playback, timers)
- Calls: VideoStream::isFrameReady, VideoStream::frameDecompress, VideoStream::frameRender, VideoStream::frameNext, TheDisplayStringManager::newDisplayString, TheDisplayStringManager::freeDisplayString

### Display::reset
- Purpose: Resets the display state
- Calls: stopMovie, View::reset

## Globals
- TheDisplay (Display*): The singleton display instance

## Dependencies
- GameClient/Display.h
- GameClient/Mouse.h
- GameClient/VideoPlayer.h
- GameClient/DisplayStringManager.h
- GameClient/GameText.h
- GameClient/GlobalLanguage.h
- PreRTS.h
- TheMouse (Mouse*)
- TheTacticalView (View*)
- TheVideoPlayer (VideoPlayer*)
- TheDisplayStringManager (DisplayStringManager*)
- TheGameText (GameText*)
- TheGlobalLanguageData (GlobalLanguageData*)
- TheFontLibrary (FontLibrary*)
- timeGetTime (function)
