# GeneralsMD/Code/GameEngine/Include/GameClient/InGameUI.h

## Purpose
Header defining the in-game user interface singleton for Command & Conquer Generals/Zero Hour.

## Responsibilities
- Manages UI elements like messages, timers, and floating text
- Handles unit selection and camera controls
- Controls placement icons and build progress
- Manages superweapon timers and military subtitles
- Provides mouse interaction and hint systems

## Key Types
- **InGameUI (Class)**: Main UI singleton managing game interface elements
- **SuperweaponInfo (Class)**: Tracks superweapon readiness and display
- **FloatingTextData (Class)**: Manages floating text above units
- **WorldAnimationData (Class)**: Handles world-space animations
- **RadiusCursorType (Enum)**: Defines different radius cursor types for abilities
- **ActionType (Enum)**: Lists possible unit actions
- **MouseMode (Enum)**: Tracks current mouse interaction state

## Key Functions
### popupMessage
- Purpose: Display popup messages to the player
- Calls: None visible in header

### message
- Purpose: Display colored messages to the player
- Calls: None visible in header

### selectUnitsMatchingCurrentSelection
- Purpose: Select units matching current selection criteria
- Calls: None visible in header

### addFloatingText
- Purpose: Add floating text above a world position
- Calls: None visible in header

### update
- Purpose: Update UI elements each frame
- Calls: None visible in header

## Globals
- **TheInGameUI (InGameUI*)**: Singleton instance of the in-game UI

## Dependencies
- Common/GameCommon.h
- Common/GameType.h
- GameClient/DisplayString.h
- GameClient/Mouse.h
- GameClient/RadiusDecal.h
- GameClient/View.h
- Forward declarations for Drawable, Object, GameWindow, etc.
