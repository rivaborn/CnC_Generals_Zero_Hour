# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindow.cpp

## Purpose
Implements the core GameWindow class, handling UI window management, input processing, and rendering callbacks.

## Responsibilities
- Manages window hierarchy (parent/child relationships)
- Handles input, system, tooltip, and draw callbacks
- Provides tab navigation between windows
- Tracks window state (enabled/disabled/hidden)
- Manages window regions and positioning

## Key Types
- **GameWindow (Class)**: Base class for all UI windows
- **WinInstanceData (Struct)**: Stores per-instance window data
- **WindowMsgHandledType (Enum)**: Return type for message handlers

## Key Functions
### GameWinBlockInput
- Purpose: Blocks mouse input (char/mouse position) and handles drag-selecting cleanup
- Calls: TheSelectionTranslator->setLeftMouseButton, setDragSelecting, TheTacticalView->setMouseLock, TheInGameUI->setSelecting, endAreaSelectHint

### winPointInChild
- Purpose: Finds the child window containing a given point
- Calls: winPointInChild recursively on children

### winPointInAnyChild
- Purpose: Finds any child window containing a point, ignoring hidden/enabled state
- Calls: winPointInChild on children

## Globals
- None

## Dependencies
- GameClient headers: WindowLayout.h, GameWindow.h, GameWindowManager.h, Gadget.h, DisplayStringManager.h, GadgetListBox.h, GadgetComboBox.h, GadgetTextEntry.h, GadgetStaticText.h, Mouse.h, SelectionXlat.h
- Common headers: AudioEventRTS.h, Language.h
- External symbols: TheWindowManager, TheAudio, TheSelectionTranslator, TheTacticalView, TheInGameUI
