# Generals/Code/GameEngine/Source/GameClient/GUI/GameWindowTransitionsStyles.cpp

## Purpose
Implements various GUI window transition effects (fades, flashes, button animations) for the game's UI system.

## Responsibilities
- Defines transition classes (Flash, ButtonFlash, FullFade, TextOnFrame, ReverseSound)
- Handles window visibility and animation states
- Manages audio events for transitions
- Renders transition effects using display primitives
- Provides button image drawing utilities

## Key Types
- `Transition` (Class): Base class for all window transitions
- `FlashTransition` (Class): Implements a flashing window transition effect
- `ButtonFlashTransition` (Class): Handles button-specific flash transitions
- `FullFadeTransition` (Class): Manages full-screen fade transitions
- `TextOnFrameTransition` (Class): Controls text display on window frames
- `ReverseSoundTransition` (Class): Plays sound effects during transitions

## Key Functions
### `FlashTransition::update`
- Purpose: Updates the flash transition state based on frame number
- Calls: `winHide`, `addAudioEvent`

### `ButtonFlashTransition::draw`
- Purpose: Renders button flash transition effects
- Calls: `winGetScreenPosition`, `winGetSize`, `GadgetButtonGetLeftEnabledImage`, etc.

### `FullFadeTransition::draw`
- Purpose: Draws full-screen fade effects
- Calls: `drawFillRect`, `drawOpenRect`

### `PushButtonImageDrawThree`
- Purpose: Draws three-part button images (left/center/right)
- Calls: `winGetScreenPosition`, `winGetSize`, `GadgetButtonGetLeftEnabledImage`, etc.

### `drawTypeText`
- Purpose: Renders text for static text gadgets
- Calls: `winGetScreenPosition`, `winGetSize`, `setWordWrap`, `draw`

## Globals
- `TheDisplay` (Display*): Global display interface for rendering
- `TheAudio` (GameAudio*): Global audio interface for sound events
- `TheMappedImageCollection` (ImageCollection*): Global image collection

## Dependencies
- `GameWindowTransitions.h`, `GameWindow.h`, `Display.h`
- `GadgetPushButton.h`, `GadgetStaticText.h`, `Controlbar.h`
- AudioEventRTS, GameAudio, DisplayString, Image classes
