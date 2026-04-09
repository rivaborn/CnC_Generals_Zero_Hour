# GeneralsMD/Code/GameEngine/Include/GameClient/ControlBarScheme.h

## Purpose
Defines classes and structures for managing control bar schemes, animations, and images in the game UI.

## Responsibilities
- Declares control bar scheme management classes
- Defines image and animation structures for UI elements
- Provides parsing infrastructure for INI configuration
- Manages control bar rendering and updates

## Key Types
- **ControlBarSchemeImage (Class)**: Holds image data for control bar elements
- **ControlBarSchemeAnimation (Class)**: Manages animated control bar elements
- **ControlBarScheme (Class)**: Contains all information for a control bar scheme
- **ControlBarSchemeManager (Class)**: Manages control bar schemes and their rendering
- **TimeOfDay (Enum)**: Time of day enum (forward reference)

## Key Functions
### ControlBarSchemeManager::parseImagePart
- Purpose: Parses image configuration from INI files
- Calls: Not inferable

### ControlBarSchemeManager::parseAnimatingPart
- Purpose: Parses animation configuration from INI files
- Calls: Not inferable

### ControlBarSchemeManager::setControlBarSchemeByPlayer
- Purpose: Selects control bar scheme based on player template
- Calls: Not inferable

## Globals
- **m_controlBarSchemeFieldParseTable (FieldParse[])**: Parse table for INI configuration

## Dependencies
- "GameClient/Color.h"
- AsciiString, playerTemplate, Image (forward references)
- TimeOfDay (forward reference)
- std::list
- INI, Player, PlayerTemplate (external types)
