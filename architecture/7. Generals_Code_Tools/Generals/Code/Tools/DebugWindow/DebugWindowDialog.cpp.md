# Generals/Code/Tools/DebugWindow/DebugWindowDialog.cpp

## Purpose
Implements a debug window dialog for the game, providing controls for stepping, pausing, and monitoring game state.

## Responsibilities
- Manages debug controls (pause, step, run fast)
- Displays debug messages and variables
- Handles window focus and sizing
- Updates UI elements based on debug state

## Key Types
- DebugWindowDialog (Class): Main dialog class for debug window
- VecPairString (Type): Vector of string pairs (variable names/values)
- VecStringIt (Type): Iterator for message strings

## Key Functions
### OnPause
- Purpose: Toggles pause state for game execution
- Calls: `_UpdatePauseButton`

### OnStep
- Purpose: Steps game execution by one frame
- Calls: `_UpdatePauseButton`

### AppendMessage
- Purpose: Adds a debug message to the display
- Calls: `_RebuildMesgString`

### AdjustVariable
- Purpose: Updates or adds a variable to the debug display
- Calls: `_RebuildVarsString`

### _UpdatePauseButton
- Purpose: Updates the pause button UI state
- Calls: None

## Globals
- None

## Dependencies
- `DebugWindowDialog.h` (header)
- MFC classes (`CDialog`, `CWnd`, `CButton`, `CEdit`)
- STL containers (`vector`, `string`)
- Windows API (`FindWindow`, `SetFocus`)
