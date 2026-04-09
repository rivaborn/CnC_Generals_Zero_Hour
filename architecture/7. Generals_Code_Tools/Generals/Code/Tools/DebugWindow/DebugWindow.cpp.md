# Generals/Code/Tools/DebugWindow/DebugWindow.cpp

## Purpose
Manages a debug window DLL for the game, providing runtime debugging utilities.

## Responsibilities
- Creates and destroys the debug window dialog
- Manages debug message logging and variable adjustment
- Controls game execution flow (pause/continue)
- Maintains global debug state

## Key Types
- CDebugWindowApp (Class): Main application class managing the debug window
- DebugWindowDialog* (Pointer): Reference to the active debug dialog window

## Key Functions
### CreateDebugDialog
- Purpose: Creates and displays the debug window dialog
- Calls: DebugWindowDialog constructor, Create, SetWindowPos, ShowWindow

### DestroyDebugDialog
- Purpose: Destroys the debug window dialog and cleans up resources
- Calls: DestroyWindow, delete operator

### CanAppContinue
- Purpose: Checks if the application can continue execution
- Calls: GetDialogWindow, CanProceed

### ForceAppContinue
- Purpose: Forces the application to continue execution
- Calls: GetDialogWindow, ForceContinue

### RunAppFast
- Purpose: Checks if the application should run at normal speed
- Calls: GetDialogWindow, RunAppFast

### AppendMessage
- Purpose: Adds a message to the debug window log
- Calls: GetDialogWindow, AppendMessage

### SetFrameNumber
- Purpose: Updates the displayed frame number in the debug window
- Calls: GetDialogWindow, SetFrameNumber

### AppendMessageAndPause
- Purpose: Logs a message and pauses execution
- Calls: GetDialogWindow, AppendMessage, ForcePause

### AdjustVariable
- Purpose: Modifies a game variable through the debug window
- Calls: GetDialogWindow, AdjustVariable

### AdjustVariableAndPause
- Purpose: Adjusts a variable and pauses execution
- Calls: GetDialogWindow, AdjustVariable, ForcePause

## Globals
- theApp (CDebugWindowApp): The singleton application instance

## Dependencies
- DebugWindow.h, DebugWindowDialog.h
- MFC framework (CWinApp, AfxManageState)
- DebugWindowDialog class methods
