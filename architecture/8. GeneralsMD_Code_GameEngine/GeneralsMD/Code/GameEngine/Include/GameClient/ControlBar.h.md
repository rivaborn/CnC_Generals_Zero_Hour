# GeneralsMD/Code/GameEngine/Include/GameClient/ControlBar.h

## Purpose
Header file defining the ControlBar system for the game's UI, including command buttons, command sets, and context-sensitive interfaces.

## Responsibilities
- Defines enums for command options, GUI commands, and control bar states
- Declares CommandButton and CommandSet classes for UI elements
- Declares ControlBar class managing the in-game control interface
- Provides forward declarations for related game classes

## Key Types
- CommandButton (Class): Represents a clickable button in the control bar with associated commands
- CommandSet (Class): Groups related command buttons for different contexts
- ControlBar (Class): Main control bar system managing UI state and command processing
- CommandOption (Enum): Bit flags for command button behavior options
- GUICommandType (Enum): Enumeration of all possible GUI commands
- ControlBarContext (Enum): Different UI contexts (command, inventory, etc.)

## Key Functions
### processContextSensitiveButtonClick
- Purpose: Handles clicks on context-sensitive command buttons
- Calls: Not visible in header

### evaluateContextUI
- Purpose: Evaluates what UI elements should be shown based on current selection
- Calls: Not visible in header

### setControlCommand
- Purpose: Sets command data into a button
- Calls: Not visible in header

## Globals
- TheControlBar (ControlBar*): Global instance of the control bar system
- CommandButtonMappedBorderTypeNames (LookupListRec[]): Mapping of border types to names

## Dependencies
- Common/AudioEventRTS.h
- Common/GameType.h
- Common/Overridable.h
- Common/Science.h
- GameClient/Color.h
- Forward declarations for Drawable, GameWindow, Object, and other game classes
