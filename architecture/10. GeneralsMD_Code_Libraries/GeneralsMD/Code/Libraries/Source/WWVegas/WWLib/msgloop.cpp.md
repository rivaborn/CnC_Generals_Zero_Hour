# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/msgloop.cpp

## Purpose
Handles Windows message processing, including accelerators and modeless dialogs.

## Responsibilities
- Processes Windows messages in a loop
- Manages modeless dialog message handling
- Tracks and applies keyboard accelerators
- Supports custom message interception

## Key Types
- **AcceleratorTracker (struct)**: Tracks window and accelerator pairs

## Key Functions
### Windows_Message_Handler
- Purpose: Processes all pending Windows messages
- Calls: `PeekMessage`, `GetMessage`, `TranslateAccelerator`, `IsDialogMessage`, `TranslateMessage`, `DispatchMessage`

### Add_Modeless_Dialog
- Purpose: Registers a modeless dialog for message handling
- Calls: `_ModelessDialogs.Add`

### Remove_Modeless_Dialog
- Purpose: Unregisters a modeless dialog
- Calls: `_ModelessDialogs.Delete`

### Add_Accelerator
- Purpose: Registers a keyboard accelerator
- Calls: `_Accelerators.Add`

### Remove_Accelerator
- Purpose: Unregisters a keyboard accelerator
- Calls: `_Accelerators.Delete`

## Globals
- `_ModelessDialogs (DynamicVectorClass<HWND>)`: Tracks active modeless dialogs
- `_Accelerators (DynamicVectorClass<AcceleratorTracker>)`: Tracks active accelerators
- `Message_Intercept_Handler (bool (*)(MSG &))`: Custom message handler function pointer

## Dependencies
- `always.h`, `vector.h`, `win.h`
- Windows API: `PeekMessage`, `GetMessage`, `TranslateAccelerator`, `IsDialogMessage`, `TranslateMessage`, `DispatchMessage`
