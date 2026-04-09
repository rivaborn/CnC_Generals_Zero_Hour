# Generals/Code/GameEngine/Source/GameClient/GUI/WindowLayout.cpp

## Purpose
Manages groups of windows (WindowLayout) for the game's GUI system, handling creation, destruction, and organization of windows.

## Responsibilities
- Maintains a linked list of GameWindow objects
- Provides methods to add/remove windows from the layout
- Handles loading window layouts from .wnd script files
- Manages visibility state for all windows in the layout
- Supports bringing all windows in the layout to the front

## Key Types
- WindowLayout (Class): Manages a collection of GameWindow objects as a group
- WindowLayoutInfo (Struct): Contains window list and callback functions from .wnd files

## Key Functions
### WindowLayout::hide
- Purpose: Shows or hides all windows in the layout
- Calls: GameWindow::winHide

### WindowLayout::addWindow
- Purpose: Adds a window to this layout's linked list
- Calls: GameWindow::winSetPrevInLayout, GameWindow::winSetNextInLayout, GameWindow::winSetLayout

### WindowLayout::removeWindow
- Purpose: Removes a window from this layout's linked list
- Calls: GameWindow::winSetPrevInLayout, GameWindow::winSetNextInLayout, GameWindow::winSetLayout

### WindowLayout::destroyWindows
- Purpose: Destroys all windows in this layout
- Calls: WindowLayout::removeWindow, TheWindowManager->winDestroy

### WindowLayout::load
- Purpose: Loads window layout from a .wnd script file
- Calls: TheWindowManager->winCreateFromScript

### WindowLayout::bringForward
- Purpose: Brings all windows in layout to the top of the window stack
- Calls: GameWindow::winBringToTop

### WindowLayout::findWindow
- Purpose: Finds a window within this layout
- Calls: None

## Globals
- None

## Dependencies
- GameClient/WindowLayout.h
- GameClient/Shell.h
- GameClient/GameWindowManager.h
- PreRTS.h
- AsciiString
- std::list
