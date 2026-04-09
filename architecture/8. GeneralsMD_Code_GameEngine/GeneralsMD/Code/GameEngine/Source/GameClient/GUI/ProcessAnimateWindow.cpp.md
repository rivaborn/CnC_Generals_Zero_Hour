# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ProcessAnimateWindow.cpp

## Purpose
Implements animation behaviors for UI windows sliding from different screen edges.

## Responsibilities
- Defines animation process classes for sliding windows from left/right/top
- Manages window movement physics (velocity, acceleration, deceleration)
- Handles initialization, updating, and reversing of animations
- Controls timing and positioning of animated windows

## Key Types
- `ProcessAnimateWindowSlideFromRight` (Class): Slides window from right edge
- `ProcessAnimateWindowSlideFromLeft` (Class): Slides window from left edge
- `ProcessAnimateWindowSlideFromTopFast` (Class): Slides window from top edge quickly
- `ProcessAnimateWindowSlideFromRightFast` (Class): Slides window from right edge quickly

## Key Functions
### `initAnimateWindow`
- Purpose: Initializes window animation parameters
- Calls: `winGetPosition`, `winGetSize`, `winSetPosition`, `setAnimData`

### `updateAnimateWindow`
- Purpose: Updates window position during animation
- Calls: `winGetPosition`, `winSetPosition`, `getCurPos`, `getEndPos`, `setCurPos`, `setVel`

### `reverseAnimateWindow`
- Purpose: Reverses window animation direction
- Calls: `winGetPosition`, `winSetPosition`, `getCurPos`, `getStartPos`, `setCurPos`, `setVel`

## Globals
- `TheDisplay` (Display*): Global display system reference

## Dependencies
- `PreRTS.h`, `ProcessAnimateWindow.h`, `AnimateWindowManager.h`, `GameWindow.h`, `Display.h`
- `AnimateWindow`, `GameWindow`, `Coord2D`, `ICoord2D` types
- `DEBUG_ASSERTCRASH`, `timeGetTime` macros/functions
