# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/AnimateWindowManager.cpp

## Purpose
Manages window animations in the game UI, handling different animation types and their lifecycle.

## Responsibilities
- Manages lists of animated windows
- Updates and reverses animations
- Registers game windows with specific animations
- Cleans up animation resources

## Key Types
- `AnimateWindow` (Class): Represents a window with animation properties
- `AnimateWindowManager` (Class): Main class managing all window animations
- `ProcessAnimateWindow` (Class): Base class for specific animation behaviors
- `AnimTypes` (Enum): Defines types of window animations

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
- None

## Dependencies
- `AnimateWindowManager.h`
- `GameWindow.h`
- `Display.h`
- `ProcessAnimateWindow.h`
- `PreRTS.h`
