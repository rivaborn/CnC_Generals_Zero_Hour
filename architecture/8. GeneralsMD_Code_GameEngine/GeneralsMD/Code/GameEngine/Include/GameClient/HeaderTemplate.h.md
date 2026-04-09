# GeneralsMD/Code/GameEngine/Include/GameClient/HeaderTemplate.h

## Purpose
Defines classes for managing header templates and fonts in the game UI.

## Responsibilities
- Declares `HeaderTemplate` class for storing font properties
- Declares `HeaderTemplateManager` for template management
- Provides font retrieval and iteration methods
- Handles resolution change notifications for headers

## Key Types
- **HeaderTemplate (Class)**: Stores font properties (name, point size, bold flag)
- **HeaderTemplateManager (Class)**: Manages header templates and fonts
- **FieldParse (Class)**: Used for parsing header fields (forward reference)
- **INI (Class)**: Used for configuration (forward reference)
- **GameFont (Class)**: Font resource (forward reference)

## Key Functions
### HeaderTemplateManager::init
- Purpose: Initializes the header template manager
- Calls: `populateGameFonts`

### HeaderTemplateManager::getFontFromTemplate
- Purpose: Retrieves a GameFont from a named template
- Calls: `findHeaderTemplate`

### HeaderTemplateManager::headerNotifyResolutionChange
- Purpose: Notifies all headers of resolution changes
- Calls: None visible

## Globals
- **TheHeaderTemplateManager (HeaderTemplateManager*)**: Singleton instance of the manager

## Dependencies
- `Common/STLTypedefs.h`, `Common/AsciiString.h`
- Forward references: `GameFont`, `FieldParse`, `INI`
- STL: `std::list`
