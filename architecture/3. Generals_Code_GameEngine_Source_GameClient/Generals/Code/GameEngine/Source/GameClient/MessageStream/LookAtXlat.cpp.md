# Generals/Code/GameEngine/Source/GameClient/MessageStream/LookAtXlat.cpp

## Purpose
Handles translation of raw input events (mouse/keyboard) into camera movement commands for the game view.

## Responsibilities
- Processes input messages (keys, mouse buttons, wheel, position)
- Manages camera scrolling, rotation, and pitch adjustments
- Handles bookmarking camera views (F-keys)
- Tracks mouse movement for recent activity checks
- Manages debug/internal demo camera controls

## Key Types
- (anonymous enum) (Enum): Direction constants (up, down, left, right)
- DIR_UP (Enum): Up direction constant
- DIR_DOWN (Enum): Down direction constant
- DIR_LEFT (Enum): Left direction constant
- DIR_RIGHT (Enum): Right direction constant

## Key Functions
### LookAtTranslator::translateGameMessage
- Purpose: Processes game messages to translate input into camera commands
- Calls: setScrolling, stopScrolling, TheTacticalView methods, TheInGameUI methods

### LookAtTranslator::setScrolling
- Purpose: Initiates camera scrolling mode
- Calls: TheInGameUI->setScrolling, TheTacticalView->setMouseLock

### LookAtTranslator::stopScrolling
- Purpose: Terminates camera scrolling mode
- Calls: TheInGameUI->setScrolling, TheTacticalView->setMouseLock, TheMouse->setCursor

### LookAtTranslator::resetModes
- Purpose: Resets all camera movement modes
- Calls: None

## Globals
- TheLookAtTranslator (LookAtTranslator*): Singleton instance of the translator
- scrollDir (Bool[4]): Tracks active scroll directions
- SCROLL_AMT (Int): Scroll amount constant
- edgeScrollSize (Int): Screen edge scroll trigger size
- prevCursor (Mouse::MouseCursor): Stores previous cursor state during scrolling

## Dependencies
- Common/GameType.h, Common/MessageStream.h, GameClient/Display.h
- GameClient/Mouse.h, GameClient/Shell.h, GameClient/GameClient.h
- GameClient/KeyDefs.h, GameClient/View.h, GameClient/LookAtXlat.h
- GameLogic/Module/UpdateModule.h, GameLogic/GameLogic.h
- Common/GlobalData.h
