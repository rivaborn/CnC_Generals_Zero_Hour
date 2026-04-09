# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGameWindowManager.h

## Purpose
Manages game windows and UI controls for the W3D rendering system in Command & Conquer Generals.

## Responsibilities
- Allocates W3D-specific game windows
- Provides draw functions for various UI gadgets
- Initializes the window manager singleton
- Returns default draw functions for UI elements

## Key Types
- W3DGameWindowManager (Class): W3D implementation of the game window manager

## Key Functions
### W3DGameWindowManager::allocateNewWindow
- Purpose: Allocates a new W3D game window
- Calls: newInstance(W3DGameWindow)

### W3DGameWindowManager::getDefaultDraw
- Purpose: Returns the default draw function for game windows
- Calls: None

### W3DGameWindowManager::getPushButtonImageDrawFunc
- Purpose: Returns the draw function for push button images
- Calls: None

### W3DGameWindowManager::getPushButtonDrawFunc
- Purpose: Returns the draw function for push buttons
- Calls: None

### W3DGameWindowManager::getCheckBoxImageDrawFunc
- Purpose: Returns the draw function for checkbox images
- Calls: None

### W3DGameWindowManager::getCheckBoxDrawFunc
- Purpose: Returns the draw function for checkboxes
- Calls: None

### W3DGameWindowManager::getRadioButtonImageDrawFunc
- Purpose: Returns the draw function for radio button images
- Calls: None

### W3DGameWindowManager::getRadioButtonDrawFunc
- Purpose: Returns the draw function for radio buttons
- Calls: None

### W3DGameWindowManager::getTabControlImageDrawFunc
- Purpose: Returns the draw
