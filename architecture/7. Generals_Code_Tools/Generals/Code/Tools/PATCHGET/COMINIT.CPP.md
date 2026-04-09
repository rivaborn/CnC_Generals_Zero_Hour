# Generals/Code/Tools/PATCHGET/COMINIT.CPP

## Purpose
Initializes and cleans up COM (Component Object Model) for the application.

## Responsibilities
- Initializes COM on object creation
- Displays error if COM initialization fails
- Uninitializes COM on object destruction
- Ensures COM cleanup via global instance

## Key Types
- ComInit (Class): RAII wrapper for COM initialization/uninitialization

## Key Functions
### ComInit::ComInit()
- Purpose: Initializes COM and shows error if failed
- Calls: `CoInitialize`, `MessageBox`, `exit`

### ComInit::~ComInit()
- Purpose: Uninitializes COM
- Calls: `CoUninitialize`

## Globals
- Global_COM_Initializer (ComInit): Ensures COM init/cleanup via static lifetime

## Dependencies
- `<windows.h>`: Windows API
- `<objbase.h>`: COM headers
- `CoInitialize`, `CoUninitialize`: COM initialization functions
- `MessageBox`, `exit`: Error handling and termination
