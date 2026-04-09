# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarMultiSelect.cpp

## Purpose
Manages the multi-select context-sensitive GUI for the control bar, showing commands common to all selected units.

## Responsibilities
- Resets common command data
- Adds common commands for selected drawables
- Populates the control bar with multi-select commands
- Updates command availability for selected units

## Key Types
- **ControlBar (Class)**: Manages the control bar GUI
- **CommandButton (Struct)**: Represents a command button
- **CommandSet (Struct)**: Contains a set of command buttons
- **Drawable (Class)**: Represents a drawable object in the game
- **Object (Class)**: Represents a game object

## Key Functions
### resetCommonCommandData
- Purpose: Clears the common command data and hides command windows
- Calls: GadgetButtonDrawOverlayImage

### addCommonCommands
- Purpose: Adds common commands for a drawable to the common command set
- Calls: findCommandSet, setControlCommand

### populateMultiSelect
- Purpose: Populates the control bar with commands common to all selected units
- Calls: resetCommonCommandData, addCommonCommands, setPortraitByObject

### updateContextMultiSelect
- Purpose: Updates the availability of commands for selected units
- Calls: getCommandAvailability, GadgetCheckLikeButtonSetVisualCheck

## Globals
- **MAX_COMMANDS_PER_SET (const Int)**: Maximum number of commands per set
- **m_commonCommands (CommandButton*)**: Array of common commands
- **m_commandWindows (GameWindow*)**: Array of command windows

## Dependencies
- PreRTS.h
- Common/ThingTemplate.h
- GameClient/ControlBar.h
- GameClient/Drawable.h
- GameClient/GameClient.h
- GameClient/GadgetPushButton.h
- GameClient/GameWindow.h
- GameClient/InGameUI.h
- GameLogic/Object.h
