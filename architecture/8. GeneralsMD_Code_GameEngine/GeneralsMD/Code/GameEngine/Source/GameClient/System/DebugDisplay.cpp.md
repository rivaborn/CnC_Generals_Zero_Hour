# GeneralsMD/Code/GameEngine/Source/GameClient/System/DebugDisplay.cpp

## Purpose
Implements the DebugDisplay class for rendering debug text in the game client.

## Responsibilities
- Manages debug text display position and formatting
- Handles text color and margins
- Processes formatted debug output with line wrapping
- Tracks cursor position within debug display area

## Key Types
- DebugDisplay (Class): manages debug text rendering state and formatting

## Key Functions
### DebugDisplay::printf
- Purpose: Formats and renders debug text with line wrapping
- Calls: vsprintf, drawText

### DebugDisplay::reset
- Purpose: Resets debug display state to defaults
- Calls: setCursorPos, setTextColor, setRightMargin, setLeftMargin

### DebugDisplay::setCursorPos
- Purpose: Updates the current text cursor position
- Calls: None

### DebugDisplay::drawText
- Purpose: Renders text at specified position (declared in header)
- Calls: Not inferable

## Globals
- None

## Dependencies
- "GameClient/DebugDisplay.h" (header)
- "PreRTS.h" (engine precompiled header)
- vsprintf (C runtime)
- DEBUG_ASSERTCRASH (engine assertion macro)
