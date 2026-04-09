# Generals/Code/Tools/DebugWindow/DebugWindowDialog.h

## Purpose
Header for a debug window dialog class used in the game's development tools.

## Responsibilities
- Manages debug messages and variable display
- Controls game execution flow (pause, step, run fast)
- Handles UI events for the debug window
- Maintains frame number tracking

## Key Types
- **PairString (typedef)**: Pair of strings for variable name/value storage
- **VecPairString (typedef)**: Vector of variable name/value pairs
- **VecString (typedef)**: Vector of strings for message storage
- **VecPairStringIt (typedef)**: Iterator for VecPairString
- **VecStringIt (typedef)**: Iterator for VecString
- **DebugWindowDialog (class)**: Main dialog class for debug window functionality

## Key Functions
### DebugWindowDialog()
- Purpose: Constructor for the debug window dialog
- Calls: None

### CanProceed()
- Purpose: Checks if game execution can proceed
- Calls: None

### RunAppFast()
- Purpose: Runs the game at normal speed
- Calls: None

### AppendMessage()
- Purpose: Adds a debug message to the message list
- Calls: None

### AdjustVariable()
- Purpose: Updates a variable's value in the debug display
- Calls: None

### SetFrameNumber()
- Purpose: Sets the current frame number
- Calls: None

### _RebuildVarsString()
- Purpose: Rebuilds the string representation of variables
- Calls: None

### _RebuildMesgString()
- Purpose: Rebuilds the string representation of messages
- Calls: None

### _UpdatePauseButton()
- Purpose: Updates the pause button state
- Calls: None

### OnPause()
- Purpose: Handles pause button click
- Calls: None

### OnStep()
