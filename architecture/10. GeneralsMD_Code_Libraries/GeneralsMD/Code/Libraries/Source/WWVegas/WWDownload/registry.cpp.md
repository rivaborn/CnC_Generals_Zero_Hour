# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/registry.cpp

## Purpose
Provides a simple interface for reading and writing string/unsigned integer values to the Windows registry under the game's registry path.

## Responsibilities
- Read/write strings from/to Windows registry
- Read/write unsigned integers from/to Windows registry
- Handle both HKEY_LOCAL_MACHINE and HKEY_CURRENT_USER registry hives
- Construct full registry paths for the game

## Key Types
None

## Key Functions
### getStringFromRegistry
- Purpose: Retrieves a string value from the registry.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### getUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the registry.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### setStringInRegistry
- Purpose: Writes a string value to the registry.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### setUnsignedIntInRegistry
- Purpose: Writes an unsigned integer value to the registry.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### GetStringFromRegistry
- Purpose: Wrapper that checks both HKEY_LOCAL_MACHINE and HKEY_CURRENT_USER for a string value.
- Calls: getStringFromRegistry

### GetUnsignedIntFromRegistry
- Purpose: Wrapper that checks both HKEY_LOCAL_MACHINE and HKEY_CURRENT_USER for an unsigned integer value.
- Calls: getUnsignedIntFromRegistry

### SetStringInRegistry
- Purpose: Wrapper that writes a string value to both HKEY_LOCAL_MACHINE and HKEY_CURRENT_USER.
- Calls: setStringInRegistry

### SetUnsignedIntInRegistry
- Purpose: Wrapper that writes an unsigned integer value to both H
