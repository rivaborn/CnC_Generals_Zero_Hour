# Generals/Code/GameEngine/Source/Common/System/registry.cpp

## Purpose
This file provides functions to interact with the Windows registry for storing and retrieving configuration settings related to Command & Conquer Generals.

## Responsibilities
- Read string values from the registry.
- Read unsigned integer values from the registry.
- Write string values to the registry.
- Write unsigned integer values to the registry.
- Provide convenience functions to access specific registry keys used by the game.

## Key Types
- None

## Key Functions
### getStringFromRegistry
- Purpose: Retrieves a string value from the Windows registry.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### getUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the Windows registry.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### setStringInRegistry
- Purpose: Writes a string value to the Windows registry.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### setUnsignedIntInRegistry
- Purpose: Writes an unsigned integer value to the Windows registry.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### GetStringFromRegistry
- Purpose: Retrieves a string value from a specific path in the registry.
- Calls: getStringFromRegistry

### GetUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from a specific path in the registry.
- Calls: getUnsignedIntFromRegistry

### GetRegistryLanguage
- Purpose: Retrieves the language setting from the registry.
- Calls: GetStringFromRegistry

### GetRegistryGameName
- Purpose: Retrieves the game name (SKU) from the registry.
- Calls: GetStringFromRegistry

### GetRegistryVersion
- Purpose: Retrieves the game version from the registry.
- Calls: GetUnsignedIntFromRegistry

### GetRegistryMapPackVersion
- Purpose: Retrieves the map pack version from the registry.
-
