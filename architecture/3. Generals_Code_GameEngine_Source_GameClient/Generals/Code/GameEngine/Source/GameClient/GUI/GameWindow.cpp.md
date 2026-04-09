# Generals/Code/GameEngine/Source/GameClient/GUI/GameWindow.cpp

## Purpose
Implements the `GameWindow` class, which manages UI windows, their hierarchy, input handling, and rendering in the SAGE engine.

## Responsibilities
- Manages window hierarchy (parent/child relationships)
- Handles input, system, tooltip, and draw callbacks
- Provides tab navigation between windows
- Tracks window regions, sizes, and states
- Supports point-in-window and point-in-child detection

## Key Types
- `GameWindow` (Class): Core UI window class managing hierarchy, input, and rendering
- `GameWinInputFunc` (Function pointer): Callback for input events
- `GameWinSystemFunc` (Function pointer): Callback for system messages
- `GameWinTooltipFunc` (Function pointer): Callback for tooltips
- `GameWinDrawFunc` (Function pointer): Callback for rendering

## Key Functions
### `GameWinDefaultInput`
- Purpose: Default input handler that ignores all messages
- Calls: None

### `GameWinBlockInput`
- Purpose: Blocks mouse input (e.g., for walls) and handles drag-selecting
- Calls: `TheSelectionTranslator->setLeftMouseButton`, `TheSelectionTranslator->setDragSelecting`, `TheTacticalView->setMouseLock`, `TheInGameUI->setSelecting`, `TheInGameUI->endAreaSelectHint`

### `GameWinDefaultSystem`
- Purpose: Default system message handler that ignores all messages
- Calls: None

### `GameWinDefaultTooltip`
- Purpose: Default tooltip handler that does nothing
- Calls: None

### `GameWinDefaultDraw`
- Purpose: Default draw handler that does nothing
- Calls: None

### `winPointInChild`
- Purpose: Finds the child window containing a given point
- Calls: Recursively calls itself for child windows

### `winPointInAnyChild`
- Purpose: Finds a child window containing a point, ignoring hidden/enabled states
- Calls: `winPointInChild`

## Globals
- None

## Dependencies
- `GameWindow.h`, `GameWindowManager.h`, `Gadget.h`, `Mouse.h`, `SelectionXlat.h`
- `AudioEventRTS`, `TheAudio`, `TheSelectionTranslator`, `TheTacticalView`, `TheInGameUI`
