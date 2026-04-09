# Generals/Code/Libraries/Source/WWVegas/WWDownload/registry.cpp

## Purpose
Provides a simple interface for reading/writing string and unsigned integer values to the Windows Registry under the "SOFTWARE\Electronic Arts\EA Games\Generals" path.

## Responsibilities
- Read/write strings from/to Windows Registry
- Read/write unsigned integers from/to Windows Registry
- Handle both HKEY_LOCAL_MACHINE and HKEY_CURRENT_USER registry hives
- Construct full registry paths by appending subpaths to the base Generals path

## Key Types
None

## Key Functions
### getStringFromRegistry
- Purpose: Retrieves a string value from the specified registry key.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### getUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the specified registry key.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### setStringInRegistry
- Purpose: Writes a string value to the specified registry key.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### setUnsignedIntInRegistry
- Purpose: Writes an unsigned integer value to the specified registry key.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### GetStringFromRegistry
- Purpose: Wrapper that reads a string value from either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER.
- Calls: getStringFromRegistry

### GetUnsignedIntFromRegistry
- Purpose: Wrapper that reads an unsigned integer value from either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER.
- Calls: getUnsignedIntFromRegistry

### SetStringInRegistry
- Purpose: Wrapper that writes a string value to either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER.
- Calls
