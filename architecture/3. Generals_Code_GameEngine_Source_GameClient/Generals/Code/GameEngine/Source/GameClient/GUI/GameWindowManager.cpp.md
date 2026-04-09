# Generals/Code/GameEngine/Source/GameClient/GUI/GameWindowManager.cpp

## Purpose
Manages the game's windowing system, including window creation, destruction, messaging, and input handling.

## Responsibilities
- Manages window hierarchy and focus
- Handles window messaging and input propagation
- Manages modal windows and input capture
- Provides utility functions for window creation and testing

## Key Types
- `GameWindowManager` (Class): Singleton manager for the windowing system
- `ModalWindow` (Struct): Represents a modal window in the stack
- `WindowMsgHandledType` (Enum): Result of message handling

## Key Functions
### `PassSelectedButtonsToParentSystem`
- Purpose: Propagates button press messages to parent window
- Calls: `winGetParent`, `winSendSystemMsg`

### `PassMessagesToParentSystem`
- Purpose: Propagates all messages to parent window
- Calls: `winGetParent`, `winSendSystemMsg`

### `testGrab`
- Purpose: Test input handler for debugging
- Calls: None

## Globals
- `TheWindowManager` (GameWindowManager*): Singleton instance
- `WindowLayoutCurrentVersion` (UnsignedInt): Current layout version
- `sendMousePosMessages` (Bool): Controls mouse position message propagation

## Dependencies
- GameWindow.h, Mouse.h, Display.h, WindowLayout.h
- Gadget-related headers (Gadget.h, GadgetListBox.h, etc.)
- Common utilities (Debug.h, Language.h)
