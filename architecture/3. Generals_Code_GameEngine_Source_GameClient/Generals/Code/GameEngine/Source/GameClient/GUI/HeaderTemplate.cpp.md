# Generals/Code/GameEngine/Source/GameClient/GUI/HeaderTemplate.cpp

## Purpose
Manages header templates for UI consistency and localization support in the game.

## Responsibilities
- Loads and parses header template definitions from INI files
- Manages a collection of header templates
- Provides font lookup based on template names
- Handles resolution changes by updating fonts

## Key Types
- **HeaderTemplate** (Class): Stores font settings (name, size, bold) for UI headers
- **HeaderTemplateManager** (Class): Manages the collection of header templates
- **m_headerFieldParseTable** (const FieldParse[]): INI parsing rules for header templates

## Key Functions
### `parseHeaderTemplateDefinition`
- Purpose: Parses a header template definition from an INI file
- Calls: `TheHeaderTemplateManager->findHeaderTemplate`, `TheHeaderTemplateManager->newHeaderTemplate`, `ini->initFromINI`

### `HeaderTemplateManager::init`
- Purpose: Initializes the header template system by loading INI files
- Calls: `ini.load`, `populateGameFonts`

### `HeaderTemplateManager::populateGameFonts`
- Purpose: Updates fonts for all templates based on current settings
- Calls: `TheGlobalLanguageData->adjustFontSize`, `TheFontLibrary->getFont`

## Globals
- **TheHeaderTemplateManager** (HeaderTemplateManager*): Singleton instance of the header template manager

## Dependencies
- `INI.h`, `Filesystem.h`, `Registry.h`, `HeaderTemplate.h`, `GameFont.h`, `GlobalLanguage.h`
- `TheFileSystem`, `TheFontLibrary`, `TheGlobalLanguageData`
