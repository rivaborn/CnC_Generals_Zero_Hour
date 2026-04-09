# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/WindowLayout.cpp

## Purpose
Manages groups of windows in the game's GUI system, handling layout creation, window management, and visibility control.

## Responsibilities
- Maintains a linked list of windows in a layout
- Provides methods to add/remove/destroy windows
- Handles loading layouts from .wnd script files
- Manages visibility state for all windows in the layout
- Supports bringing all windows in the layout to the front

## Key Types
- WindowLayout (Class): Manages a collection of GameWindow objects and their layout behavior
- WindowLayoutInfo (Struct): Contains script loading results (not shown in this file)

## Key Functions
### WindowLayout::hide
- Purpose: Shows or hides all windows in the layout
- Calls: GameWindow::winHide

### WindowLayout::addWindow
- Purpose: Adds a window to the layout's linked list
- Calls: findWindow, GameWindow::winSetPrevInLayout, GameWindow::winSetNextInLayout, GameWindow::winSetLayout

### WindowLayout::removeWindow
- Purpose: Removes a window from the layout's linked list
- Calls: findWindow, GameWindow::winSetPrevInLayout, GameWindow::winSetNextInLayout, GameWindow::winSetLayout

### WindowLayout::destroyWindows
- Purpose: Destroys all windows in the layout
- Calls: getFirstWindow, removeWindow, TheWindowManager->winDestroy

### WindowLayout::load
- Purpose: Loads a window layout from a .wnd script file
- Calls: TheWindowManager->winCreateFromScript, addWindow, setInit, setUpdate, setShutdown

### WindowLayout::bringForward
- Purpose: Brings all windows in the layout to the top of the window stack
- Calls: GameWindow::winBringToTop

### WindowLayout::findWindow
- Purpose: Finds a window in the layout's linked list
- Calls: None

## Globals
- None

## Dependencies
- GameClient/WindowLayout.h
- GameClient/Shell.h
- GameClient/GameWindowManager.h
- PreRTS.h
- AsciiString
- Bool
- Int
- std::list
- TheWindowManager (external symbol)
