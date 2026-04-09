# GeneralsMD/Code/GameEngine/Source/Common/System/registry.cpp

## Purpose
Provides a simple interface for storing and retrieving registry values in Windows.

## Responsibilities
- Read/write string and unsigned integer values from/to Windows registry
- Handle registry keys under specific EA/Generals paths
- Cache certain registry values (e.g., language) for performance
- Provide convenience functions for common game settings

## Key Types
None

## Key Functions
### getStringFromRegistry
- Purpose: Retrieves a string value from the Windows registry
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### getUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the Windows registry
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### setStringInRegistry
- Purpose: Writes a string value to the Windows registry
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### setUnsignedIntInRegistry
- Purpose: Writes an unsigned integer value to the Windows registry
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### GetStringFromGeneralsRegistry
- Purpose: Retrieves a string value from the Generals-specific registry path
- Calls: getStringFromRegistry

### GetStringFromRegistry
- Purpose: Retrieves a string value from the Zero Hour-specific registry path
- Calls: getStringFromRegistry

### GetUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the Zero Hour-specific registry path
- Calls: getUnsignedIntFromRegistry

### GetRegistryLanguage
- Purpose: Gets the cached or current game language setting
- Calls: GetStringFromRegistry

### GetRegistryGameName
- Purpose: Gets the game SKU identifier
- Calls: GetStringFromRegistry
