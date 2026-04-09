# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGameWindowManager.h

## Purpose
Manages W3D-specific game window and UI control rendering for the in-game GUI system.

## Responsibilities
- Provides factory methods for creating W3D game windows
- Returns draw function pointers for various UI control types
- Initializes the window manager singleton
- Bridges between generic GameWindowManager and W3D rendering

## Key Types
- W3DGameWindowManager (Class): W3D implementation of the game window manager

## Key Functions
### allocateNewWindow
- Purpose: Creates a new W3D game window instance
- Calls: newInstance(W3DGameWindow)

### getDefaultDraw
- Purpose: Returns the default window drawing function
- Calls: None

### getPushButtonImageDrawFunc / getPushButtonDrawFunc / ... / getTextEntryDrawFunc
- Purpose: Returns draw function pointers for specific UI control types
- Calls: None (inline return of global function pointers)

## Globals
- None

## Dependencies
- GameClient/GameWindowManager.h
- W3DDevice/GameClient/W3DGameWindow.h
- W3DDevice/GameClient/W3DGadget.h
- W3DGameWinDefaultDraw, W3DGadgetPushButtonImageDraw, etc. (external function pointers)
