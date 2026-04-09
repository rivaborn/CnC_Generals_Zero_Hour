# Generals/Code/GameEngine/Source/GameClient/GUI/ProcessAnimateWindow.cpp

## Purpose
Implements animation behaviors for UI windows (sliding from left/right/top) in the game's GUI system.

## Responsibilities
- Defines animation process classes for window transitions
- Manages window movement physics (velocity, acceleration)
- Handles initialization and updating of animated windows
- Supports reverse animations (closing windows)

## Key Types
- `ProcessAnimateWindowSlideFromRight` (Class): Slides window from right edge
- `ProcessAnimateWindowSlideFromLeft` (Class): Slides window from left edge
- `ProcessAnimateWindowSlideFromTopFast` (Class): Fast vertical slide from top
- `ProcessAnimateWindowSlideFromRightFast` (Class): Fast horizontal slide from right

## Key Functions
### `initAnimateWindow`
- Purpose: Sets up initial animation parameters for a window
- Calls: `winGetPosition`, `winGetSize`, `winSetPosition`, `setAnimData`

### `updateAnimateWindow`
- Purpose: Updates window position during animation frame
- Calls: `winSetPosition`, `setCurPos`, `setVel`, `isFinished`, `getStartTime`

### `reverseAnimateWindow`
- Purpose: Handles window closing animation (reverse of opening)
- Calls: `winSetPosition`, `setCurPos`, `setVel`, `setFinished`

## Globals
- `TheDisplay` (Display*): Global display system reference

## Dependencies
- `ProcessAnimateWindow.h`
- `AnimateWindowManager.h`
- `GameWindow.h`
- `Display.h`
- `PreRTS.h`
