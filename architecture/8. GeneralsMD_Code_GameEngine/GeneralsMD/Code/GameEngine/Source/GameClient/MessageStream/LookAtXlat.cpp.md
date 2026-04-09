# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/LookAtXlat.cpp

## Purpose
Handles translation of raw input events (mouse/keyboard) into camera movement commands for the game view.

## Responsibilities
- Processes input messages (keys, mouse buttons, mouse movement, wheel)
- Manages camera scrolling, rotation, pitching, and zoom
- Handles bookmarking camera views (F-keys)
- Tracks mouse movement for recent activity checks
- Manages edge-based scrolling in fullscreen mode

## Key Types
- (anonymous enum) (Enum): Direction constants (up, down, left, right)
- DIR_UP (Enum): Direction constant for up
- DIR_DOWN (Enum): Direction constant for down
- DIR_LEFT (Enum): Direction constant for left
- DIR_RIGHT (Enum): Direction constant for right

## Key Functions
### LookAtTranslator::translateGameMessage
- Purpose: Processes game messages to translate input into camera commands
- Calls: setScrolling, stopScrolling, TheTacticalView methods, TheInGameUI methods

### LookAtTranslator::setScrolling
- Purpose: Initiates camera scrolling based on input type
- Calls: TheInGameUI->setScrolling, TheTacticalView->setMouseLock

### LookAtTranslator::stopScrolling
- Purpose: Stops active camera scrolling
- Calls: TheInGameUI->setScrolling, TheTacticalView->setMouseLock, TheMouse->setCursor

### LookAtTranslator::resetModes
- Purpose: Resets all camera movement modes to false
- Calls: None

## Globals
- TheLookAtTranslator (LookAtTranslator*): Singleton instance of the translator
- scrollDir[4] (Bool[]): Tracks which directional keys are pressed
- SCROLL_AMT (Int): Amount to scroll per frame
- edgeScrollSize (Int): Size of edge region for edge-based scrolling
- prevCursor (Mouse::MouseCursor): Stores previous cursor state during scrolling

## Dependencies
- Common/GameType.h, Common/MessageStream.h, Common/Player.h
- GameClient/Display.h, GameClient/GameText.h, GameClient/Mouse.h
- GameClient/Shell.h, GameClient/GameClient.h, GameClient/KeyDefs.h
- GameClient/View.h, GameClient/Drawable.h, GameClient/LookAtXlat.h
- GameLogic/Object.h, GameLogic/PartitionManager.h
- Common/GlobalData.h
