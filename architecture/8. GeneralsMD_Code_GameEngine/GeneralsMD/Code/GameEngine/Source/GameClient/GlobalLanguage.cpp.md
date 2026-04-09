# GeneralsMD/Code/GameEngine/Source/GameClient/GlobalLanguage.cpp

## Purpose
Manages language-specific resources and font configurations for the game client.

## Responsibilities
- Loads and parses language-specific INI files
- Manages font resources (loading/unloading)
- Adjusts font sizes based on screen resolution
- Provides global access to language data via singleton

## Key Types
- **GlobalLanguage (Class)**: Main class handling language and font data
- **FontDesc (Struct)**: Describes font properties (name, size, bold)
- **TheGlobalLanguageData (GlobalLanguage*)**: Singleton instance

## Key Functions
### `INI::parseLanguageDefinition`
- Purpose: Parses language definitions from INI file
- Calls: `ini->initFromINI`

### `GlobalLanguage::init`
- Purpose: Initializes language data and loads fonts
- Calls: `ini.load`, `AddFontResource`, `GetRegistryLanguage`, `doesFileExist`

### `GlobalLanguage::parseFontDesc`
- Purpose: Parses font description from INI
- Calls: `ini->getNextQuotedAsciiString`, `ini->scanInt`, `ini->scanBool`

### `GlobalLanguage::adjustFontSize`
- Purpose: Adjusts font size based on resolution
- Calls: None (uses global `TheGlobalData`)

## Globals
- **TheGlobalLanguageData (GlobalLanguage*)**: Singleton instance
- **TheGlobalLanguageDataFieldParseTable (FieldParse[])**: INI parsing rules

## Dependencies
- `INI.h`, `Registry.h`, `GlobalLanguage.h`, `Filesystem.h`
- `AddFontResource`, `GetRegistryLanguage`, `TheGlobalData`
