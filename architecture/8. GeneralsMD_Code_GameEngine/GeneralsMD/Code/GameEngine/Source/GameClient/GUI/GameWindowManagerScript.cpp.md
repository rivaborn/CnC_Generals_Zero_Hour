# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindowManagerScript.cpp

## Purpose
Parses window definition files (.wnd) to create UI elements in the game.

## Responsibilities
- Parses window layout scripts into GameWindow objects
- Handles nested window hierarchies via a stack
- Processes visual properties (colors, fonts) and callbacks
- Manages default UI states and draw data
- Supports versioned file formats (v2+ with layout blocks)

## Key Types
- **LayoutScriptParse (Struct)**: Maps script commands to parsing functions
- **GameWindowParse (Struct)**: Links database fields to parsing routines
- **WindowStatusNames (Array)**: String representations of window status flags
- **WindowStyleNames (Array)**: String representations of window styles
- **windowStack (Array)**: Tracks parent/child window relationships

## Key Functions
### parseWindow
- Purpose: Main entry for parsing window definitions from files
- Calls: parseChildWindows, createWindow, resetWindowStack

### parseLayoutBlock
- Purpose: Parses layout-specific directives (init/update/shutdown)
- Calls: parseInit, parseUpdate, parseShutdown

### createWindow
- Purpose: Instantiates a GameWindow from parsed data
- Calls: setWindowText, parseScreenRect, parseStatus

### parseBitString
- Purpose: Converts flag strings (e.g., "A+B+C") to bitfields
- Calls: parseBitFlag

### parseColor/parseDefaultColor
- Purpose: Parses color definitions from script
- Calls: scanUnsignedInt

## Globals
- **defEnabledColor (Color)**: Default enabled state color
- **defFont (GameFont**)**: Default font for UI elements
- **windowStack (GameWindow**)**: Stack tracking window hierarchy
- **WindowStatusNames (const char**)**: Status flag strings
- **WindowStyleNames (const char**)**: Style flag strings

## Dependencies
- **Common/File.h**: File I/O operations
- **GameClient/WindowLayout.h**: Window layout management
- **GameClient/Gadget.h**: UI gadget definitions
- **Common/FunctionLexicon.h**: Function name resolution
- **GameClient/GameText.h**: Text rendering support
