# GeneralsMD/Code/GameEngine/Include/GameClient/GameWindow.h

## Purpose
Header defining the game windowing system for GUI elements in Command & Conquer Generals.

## Responsibilities
- Declares `GameWindow` class and related types for UI management
- Defines window messages, status flags, and callback types
- Provides window hierarchy and layout management
- Declares default callback functions for windows

## Key Types
- **GameWindow (Class)**: Base class for all UI windows and controls
- **WindowLayout (Class)**: Manages groups of windows as screens
- **GameFont (Class)**: Font handling for window text
- **GameWindowEditData (Struct)**: Editor-specific window data
- **GameWindowMessage (Enum)**: Window event types (mouse, keyboard, etc.)
- **WinInputReturnCode (Enum)**: Input handling return codes
- **WindowStatusNames/WindowStyleNames (Arrays)**: Status/Style flag names

## Key Functions
### GameWinDefaultDraw
- Purpose: Default window drawing callback
- Calls: None visible

### GameWinDefaultSystem
- Purpose: Default system message handler
- Calls: None visible

### GameWinDefaultInput
- Purpose: Default input event handler
- Calls: None visible

### GameWinBlockInput
- Purpose: Blocks all input for a window
- Calls: None visible

### GameWinDefaultTooltip
- Purpose: Default tooltip display handler
- Calls: None visible

## Globals
- **WindowStatusNames (const char**)**: Array of window status flag names
- **WindowStyleNames (const char**)**: Array of window style flag names

## Dependencies
- `Lib/BaseType.h`, `Common/GameMemory.h`, `GameClient/Image.h`, `GameClient/DisplayString.h`, `GameClient/WinInstanceData.h`, `GameClient/Color.h`
- `MemoryPoolObject`, `IRegion2D`, `ICoord2D`, `UnicodeString`, `AsciiString`
