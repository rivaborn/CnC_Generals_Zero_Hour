# Generals/Code/GameEngine/Source/GameClient/System/DebugDisplay.cpp

## Purpose
Implements the DebugDisplay class for rendering debug text in the game.

## Responsibilities
- Manages debug text rendering position and formatting
- Handles text color, margins, and cursor position
- Processes formatted debug output with line wrapping
- Provides accessors for display dimensions and cursor position

## Key Types
- DebugDisplay (Class): manages debug text display state and rendering

## Key Functions
### DebugDisplay::printf
- Purpose: Formats and renders debug text with line wrapping
- Calls: vsprintf, drawText

### DebugDisplay::reset
- Purpose: Resets display state to defaults
- Calls: setCursorPos, setTextColor, setRightMargin, setLeftMargin

### DebugDisplay::setCursorPos
- Purpose: Updates the current text cursor position
- Calls: None

### DebugDisplay::setTextColor
- Purpose: Sets the color for subsequent debug text
- Calls: None

### DebugDisplay::setRightMargin
- Purpose: Sets the right margin position
- Calls: None

### DebugDisplay::setLeftMargin
- Purpose: Sets the left margin position
- Calls: None

## Globals
- None

## Dependencies
- "GameClient/DebugDisplay.h" (header)
- "PreRTS.h" (precompiled header)
- vsprintf (C runtime)
- DEBUG_ASSERTCRASH (assert macro)
- Color type (from DebugDisplay.h)
- Char type (from DebugDisplay.h)
- Int type (from DebugDisplay.h)
- drawText function (external)
