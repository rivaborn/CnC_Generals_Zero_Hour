# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindowManager.cpp

## Purpose
Manages the game's windowing system, including window creation, destruction, messaging, and input handling.

## Responsibilities
- Manages window hierarchy and focus
- Handles window messaging and input propagation
- Manages modal windows and input capture
- Provides utility functions for window creation and testing

## Key Types
- GameWindowManager (Class): Singleton manager for the windowing system
- ModalWindow (Struct): Represents a modal window in the stack
- None: No other key types defined in this file

## Key Functions
### PassSelectedButtonsToParentSystem
- Purpose: Propagates button press messages to parent window
- Calls: TheWindowManager->winSendSystemMsg

### PassMessagesToParentSystem
- Purpose: Propagates all messages to parent window
- Calls: TheWindowManager->winSendSystemMsg

### testGrab
- Purpose: Test input handler for debugging
- Calls: None

## Globals
- TheWindowManager (GameWindowManager*): Singleton instance of the window manager
- WindowLayoutCurrentVersion (UnsignedInt): Version number for window layout
- sendMousePosMessages (Bool): Flag to control mouse position message propagation

## Dependencies
- GameWindowManager.h, GameWindow.h, Mouse.h, DisplayStringManager.h, WindowLayout.h
- Gadget.h and various gadget-specific headers
- Common headers: Debug.h, Language.h, NameKeyGenerator.h
- GameWindowTransitions.h for transition handling
