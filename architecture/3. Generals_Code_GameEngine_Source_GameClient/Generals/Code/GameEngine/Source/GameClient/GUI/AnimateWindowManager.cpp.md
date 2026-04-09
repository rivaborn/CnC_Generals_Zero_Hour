# Generals/Code/GameEngine/Source/GameClient/GUI/AnimateWindowManager.cpp

## Purpose
Manages window animations in the game UI, handling different animation types and their lifecycle.

## Responsibilities
- Manages lists of animated windows
- Updates and reverses animations
- Registers game windows with specific animations
- Cleans up animation resources

## Key Types
- `AnimateWindow` (Class): Represents an animated window with position, velocity, and animation state
- `AnimateWindowManager` (Class): Main class managing all window animations
- `AnimTypes` (Enum): Defines types of window animations (e.g., slide right, spiral)
- `ProcessAnimateWindow` (Class): Base class for specific animation behaviors

## Key Functions
### `clearWinList`
- Purpose: Clears and deletes all windows in an animation list
- Calls: `deleteInstance()` on each window

### `registerGameWindow`
- Purpose: Registers a game window with a specific animation type
- Calls: `newInstance()`, `setGameWindow()`, `setAnimType()`, `initAnimateWindow()`

### `update`
- Purpose: Updates all active window animations
- Calls: `getProcessAnimate()`, `updateAnimateWindow()`, `reverseAnimateWindow()`

### `reverseAnimateWindow`
- Purpose: Reverses all active animations
- Calls: `getProcessAnimate()`, `initReverseAnimateWindow()`

## Globals
- `m_slideFromRight` (ProcessAnimateWindow*): Animation processor for sliding from right
- `m_winList` (AnimateWindowList): List of windows with non-critical animations
- `m_needsUpdate` (Bool): Flag indicating if updates are needed

## Dependencies
- `AnimateWindowManager.h`, `GameWindow.h`, `Display.h`, `ProcessAnimateWindow.h`
- `DEBUG_CRASH` macro for error handling
- `newInstance` and `deleteInstance` memory management functions
