# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGUICallbacks.h

## Purpose
Header file declaring GUI rendering callbacks for W3D (W3D Game Engine) UI elements in Command & Conquer Generals.

## Responsibilities
- Declares callback functions for various UI components (HUD, menus, command bar, etc.)
- Defines forward declarations for GUI-related classes
- Provides initialization function for main menu layout

## Key Types
- GameWindow (Class): Represents a GUI window in the game
- WindowLayout (Class): Manages the layout of GUI windows
- WinInstanceData (Class): Contains instance-specific data for windows

## Key Functions
### W3DLeftHUDDraw
- Purpose: Renders the left side of the HUD
- Calls: Not inferable

### W3DMainMenuDraw
- Purpose: Renders the main menu
- Calls: Not inferable

### W3DCommandBarGridDraw
- Purpose: Renders the grid for the command bar
- Calls: Not inferable

### W3DMainMenuInit
- Purpose: Initializes the main menu layout
- Calls: Not inferable

## Globals
- None

## Dependencies
- Key includes: None (header-only)
- External symbols: GameWindow, WindowLayout, WinInstanceData (forward declarations)
