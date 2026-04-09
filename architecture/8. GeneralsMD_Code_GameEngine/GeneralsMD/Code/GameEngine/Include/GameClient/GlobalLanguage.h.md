# GeneralsMD/Code/GameEngine/Include/GameClient/GlobalLanguage.h

## Purpose
Manages language-specific global data for the game, including font configurations and text display settings.

## Responsibilities
- Stores font descriptions for various UI elements
- Handles font size adjustments based on resolution
- Manages lists of local font files
- Provides parsing functions for INI configuration
- Implements subsystem interface for initialization/reset

## Key Types
- **GlobalLanguage (Class)**: Main class managing language-specific global data
- **AsciiString (Class)**: Used for string storage (forward declared)
- **StringList (Class)**: Typedef for list of font filenames
- **StringListIt (Class)**: Typedef for StringList iterator

## Key Functions
### GlobalLanguage::adjustFontSize
- Purpose: Adjusts font size based on current resolution
- Calls: None visible

### GlobalLanguage::parseFontFileName
- Purpose: Parses font filenames from INI configuration
- Calls: None visible

### GlobalLanguage::parseFontDesc
- Purpose: Parses font descriptions from INI configuration
- Calls: None visible

## Globals
- **TheGlobalLanguageData (GlobalLanguage*)**: Global instance of the language data manager

## Dependencies
- Common/SubsystemInterface.h
- Common/STLTypedefs.h
- GameClient/FontDesc.h
- AsciiString class (forward declared)
- INI class (used in parsing functions)
