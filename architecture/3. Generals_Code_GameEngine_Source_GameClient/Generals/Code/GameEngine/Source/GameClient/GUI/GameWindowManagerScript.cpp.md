# Generals/Code/GameEngine/Source/GameClient/GUI/GameWindowManagerScript.cpp

## Purpose
Parses window definition files (.wnd) to create UI elements in the game.

## Responsibilities
- Parses window layout scripts into GameWindow objects
- Handles nested window hierarchies via a stack
- Processes various UI element properties (colors, fonts, callbacks)
- Manages default visual properties for UI elements
- Supports versioned layout files with init/update/shutdown callbacks

## Key Types
- **LayoutScriptParse (Struct)**: Maps layout block keywords to parsing functions
- **GameWindowParse (Struct)**: Maps window field names to parsing functions
- **WindowStatusNames (Array)**: String representations of window status flags
- **WindowStyleNames (Array)**: String representations of window styles
- **windowStack (Array)**: Stack tracking parent/child window relationships

## Key Functions
### parseWindow
- Purpose: Parses a complete window definition from file
- Calls: parseChildWindows, createWindow, parseLayoutBlock

### parseLayoutBlock
- Purpose: Parses layout-level directives (init/update/shutdown)
- Calls: parseInit, parseUpdate, parseShutdown

### createWindow
- Purpose: Creates a GameWindow instance from parsed data
- Calls: setWindowText, parseScreenRect, parseStatus, parseStyle

### parseBitString
- Purpose: Converts flag strings to bitfields
- Calls: parseBitFlag

### parseColor
- Purpose: Parses color values from script
- Calls: None (direct parsing)

## Globals
- **defEnabledColor (Color)**: Default enabled state color
- **defFont (GameFont**)**: Default font for windows
- **windowStack (GameWindow**)**: Stack for nested window parsing
- **WindowStatusNames (const char**)**: Status flag name lookup table
- **WindowStyleNames (const char**)**: Style name lookup table

## Dependencies
- Common/Debug.h, Common/File.h, GameClient/WindowLayout.h
- GameClient/GameWindowManager.h, GameClient/Gadget.h
- FunctionLexicon for callback resolution
- NameKeyGenerator for string-to-key conversion
