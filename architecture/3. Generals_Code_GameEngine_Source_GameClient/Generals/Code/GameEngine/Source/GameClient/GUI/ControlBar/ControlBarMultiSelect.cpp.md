# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarMultiSelect.cpp

## Purpose
Manages the multi-select context-sensitive GUI for the control bar, showing commands common to all selected units.

## Responsibilities
- Resets and populates common command data for selected units
- Updates command availability based on selected units
- Handles portrait display for selected units
- Filters out ignored GUI objects

## Key Types
- **ControlBar (Class)**: Manages control bar behavior including multi-select commands
- **CommandButton (Struct)**: Represents a command button with options and type
- **CommandSet (Class)**: Contains command buttons for an object type
- **Drawable (Class)**: Game object with visual representation
- **Object (Class)**: Game logic entity

## Key Functions
### resetCommonCommandData
- Purpose: Clears all common commands and their overlays
- Calls: `GadgetButtonDrawOverlayImage`

### addCommonCommands
- Purpose: Adds commands common to selected drawables to the control bar
- Calls: `findCommandSet`, `setControlCommand`

### populateMultiSelect
- Purpose: Populates the control bar with commands common to all selected units
- Calls: `resetCommonCommandData`, `addCommonCommands`, `setPortraitByObject`

### updateContextMultiSelect
- Purpose: Updates command availability based on selected units' capabilities
- Calls: `getCommandAvailability`, `GadgetCheckLikeButtonSetVisualCheck`

## Globals
- **MAX_COMMANDS_PER_SET (const Int)**: Maximum number of commands per set (not shown in code)
- **m_commonCommands (CommandButton*)**: Array of common commands
- **m_commandWindows (GameWindow*)**: Array of command windows

## Dependencies
- `PreRTS.h`, `ThingTemplate.h`, `ControlBar.h`, `Drawable.h`, `GameClient.h`, `GadgetPushButton.h`, `GameWindow.h`, `InGameUI.h`, `Object.h`
- `TheInGameUI` (global InGameUI instance)
- `KINDOF_IGNORED_IN_GUI` (object kind flag)
- `OBJECT_STATUS_SOLD` (object status bit)
- `GUI_COMMAND_ATTACK_MOVE` (command type constant)
- `OK_FOR_MULTI_SELECT`, `CHECK_LIKE` (command option bits)
- `WIN_STATUS_NOT_READY`, `WIN_STATUS_ALWAYS_COLOR` (window status flags)
