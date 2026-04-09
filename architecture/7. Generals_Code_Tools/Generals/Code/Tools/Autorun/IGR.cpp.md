# Generals/Code/Tools/Autorun/IGR.cpp

## Purpose
Handles reading and writing IGR (Internet Game Registry) settings from the Windows registry.

## Responsibilities
- Read IGR options from registry on initialization
- Provide accessor methods for specific IGR flags
- Write updated IGR options back to registry
- Manage registry key creation if missing

## Key Types
- `IGROptionsClass` (Class): Manages IGR registry settings
- `IGROptionsType` (Enum): Bit flags for IGR options (not shown in snippet)

## Key Functions
### `IGROptionsClass::Init`
- Purpose: Reads IGR options from registry
- Calls: `RegOpenKeyEx`, `RegQueryValueEx`, `RegCloseKey`

### `IGROptionsClass::Is_Auto_Login_Allowed`
- Purpose: Checks if auto-login is permitted
- Calls: None

### `IGROptionsClass::Is_Storing_Nicks_Allowed`
- Purpose: Checks if storing nicknames is permitted
- Calls: None

### `IGROptionsClass::Is_Running_Reg_App_Allowed`
- Purpose: Checks if running registry app is permitted
- Calls: None

### `IGROptionsClass::Set_Options`
- Purpose: Writes IGR options to registry
- Calls: `RegOpenKeyEx`, `RegCreateKeyEx`, `RegSetValueEx`, `RegCloseKey`, `Init`

## Globals
- `OnlineOptions` (`IGROptionsClass*`): Global instance of IGR options manager

## Dependencies
- Windows Registry API (`windows.h`, `winreg.h`)
- `IGR.h` (header with constants and types)
