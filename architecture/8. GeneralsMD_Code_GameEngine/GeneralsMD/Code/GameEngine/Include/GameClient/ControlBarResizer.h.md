# GeneralsMD/Code/GameEngine/Include/GameClient/ControlBarResizer.h

## Purpose
Header file defining classes for resizing control bars in the game UI.

## Responsibilities
- Define `ResizerWindow` class to store window dimensions and positions
- Define `ControlBarResizer` class to manage control bar resizing
- Provide parsing infrastructure for control bar configuration
- Manage lists of resizable windows

## Key Types
- **ResizerWindow (Class)**: Stores name, default/alternate size and position for a resizable window
- **ControlBarResizer (Class)**: Manages control bar resizing functionality
- **ResizerWindowList (Class)**: Typedef for list of `ResizerWindow` pointers

## Key Functions
### ControlBarResizer::init
- Purpose: Initialize the control bar resizer
- Calls: Not inferable

### ControlBarResizer::getFieldParse
- Purpose: Return the parsing field table for INI file parsing
- Calls: None

### ControlBarResizer::findResizerWindow
- Purpose: Find a resizer window by name
- Calls: None

### ControlBarResizer::newResizerWindow
- Purpose: Create a new resizer window
- Calls: None

### ControlBarResizer::sizeWindowsDefault
- Purpose: Size windows using default dimensions
- Calls: None

### ControlBarResizer::sizeWindowsAlt
- Purpose: Size windows using alternate dimensions
- Calls: None

## Globals
- **m_controlBarResizerParseTable (FieldParse array)**: Parse table for INI file parsing

## Dependencies
- `AsciiString` class
- `ICoord2D` class
- `FieldParse` class
- `std::list` container
- INI file parsing infrastructure
