# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindowTransitionsStyles.cpp

## Purpose
Implements various GUI window transition effects (fades, flashes, button animations) for the game's UI system.

## Responsibilities
- Defines transition classes (FlashTransition, ButtonFlashTransition, etc.)
- Handles window visibility and animation states
- Manages audio events for transitions
- Renders transition effects using display primitives
- Provides button image drawing utilities

## Key Types
- `Transition` (Class): Base class for all window transitions
- `FlashTransition` (Class): Implements fade-in/out effects
- `ButtonFlashTransition` (Class): Handles button-specific animations
- `FullFadeTransition` (Class): Full-screen fade transitions
- `TextOnFrameTransition` (Class): Text display transitions
- `ReverseSoundTransition` (Class): Sound-based transitions

## Key Functions
### `FlashTransition::update`
- Purpose: Updates transition state based on frame number
- Calls: `winHide`, `addAudioEvent`

### `ButtonFlashTransition::draw`
- Purpose: Renders button flash effects
- Calls: `winGetScreenPosition`, `winGetSize`, `drawImage`

### `PushButtonImageDrawThree`
- Purpose: Draws three-part button images (left/center/right)
- Calls: `GadgetButtonGetLeftEnabledImage`, `drawImage`, `setClipRegion`

### `drawTypeText`
- Purpose: Renders text with word wrapping and centering
- Calls: `getFont`, `setWordWrap`, `draw`

## Globals
- `TheDisplay` (Display*): Global display interface
- `TheAudio` (GameAudio*): Global audio interface
- `TheMappedImageCollection` (ImageCollection*): Global image collection

## Dependencies
- `GameWindowTransitions.h`, `GameWindow.h`, `Display.h`
- `AudioEventRTS`, `GameAudio`, `DisplayString`
- `GadgetPushButton.h`, `GadgetStaticText.h`
