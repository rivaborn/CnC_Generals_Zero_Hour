# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/HeaderTemplate.cpp

## Purpose
Manages header templates for UI consistency and localization support in the game.

## Responsibilities
- Loads and parses header template definitions from INI files
- Manages a collection of header templates
- Provides font retrieval based on template specifications
- Handles resolution changes by updating fonts

## Key Types
- **HeaderTemplate** (Class): Stores font name, size, and style for a header
- **HeaderTemplateManager** (Class): Manages the collection of header templates
- **m_headerFieldParseTable** (FieldParse[]): INI parsing table for header template fields

## Key Functions
### `parseHeaderTemplateDefinition`
- Purpose: Parses a header template definition from an INI file
- Calls: `TheHeaderTemplateManager->findHeaderTemplate`, `TheHeaderTemplateManager->newHeaderTemplate`, `ini->initFromINI`

### `HeaderTemplateManager::init`
- Purpose: Initializes the header template manager by loading INI files
- Calls: `ini.load`, `populateGameFonts`

### `HeaderTemplateManager::populateGameFonts`
- Purpose: Updates fonts for all header templates based on current settings
- Calls: `TheGlobalLanguageData->adjustFontSize`, `TheFontLibrary->getFont`

## Globals
- **TheHeaderTemplateManager** (HeaderTemplateManager*): Global instance of the header template manager

## Dependencies
- `INI`, `Filesystem`, `Registry`, `HeaderTemplate.h`, `GameFont.h`, `GlobalLanguage.h`
