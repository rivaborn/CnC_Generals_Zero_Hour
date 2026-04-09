# GeneralsMD/Code/GameEngine/Include/GameClient/ProcessAnimateWindow.h

## Purpose
Defines animation process classes for window transitions in the game UI.

## Responsibilities
- Declares base `ProcessAnimateWindow` class and derived animation types
- Provides virtual methods for window animation lifecycle (init, update, reverse)
- Manages animation parameters (velocity, thresholds, timing)

## Key Types
- **ProcessAnimateWindow (Class)**: Abstract base for window animations
- **ProcessAnimateWindowSlideFromRight (Class)**: Slides window from right edge
- **ProcessAnimateWindowSlideFromLeft (Class)**: Slides window from left edge
- **ProcessAnimateWindowSlideFromTop (Class)**: Slides window from top edge
- **ProcessAnimateWindowSlideFromTopFast (Class)**: Fast top-edge slide
- **ProcessAnimateWindowSlideFromBottom (Class)**: Slides window from bottom
- **ProcessAnimateWindowSpiral (Class)**: Spiral animation for windows
- **ProcessAnimateWindowSlideFromBottomTimed (Class)**: Timed bottom slide
- **ProcessAnimateWindowSlideFromRightFast (Class)**: Fast right-edge slide

## Key Functions
### `initAnimateWindow`
- Purpose: Initialize animation parameters for a window
- Calls: None (pure virtual)

### `updateAnimateWindow`
- Purpose: Update window position/state each frame
- Calls: None (pure virtual)

### `reverseAnimateWindow`
- Purpose: Reverse animation (e.g., close window)
- Calls: None (pure virtual)

### `setMaxDuration`
- Purpose: Set maximum animation duration (overridable)
- Calls: None

## Globals
- None

## Dependencies
- `BaseType.h` (for types like `Bool`, `UnsignedInt`, `Real`)
- Forward declarations: `AnimateWindow`, `GameWindow`
