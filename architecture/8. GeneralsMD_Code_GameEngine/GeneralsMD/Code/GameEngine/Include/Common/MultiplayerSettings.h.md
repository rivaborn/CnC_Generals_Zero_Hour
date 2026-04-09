# GeneralsMD/Code/GameEngine/Include/Common/MultiplayerSettings.h

## Purpose
Defines multiplayer game settings including colors, starting money, and game rules.

## Responsibilities
- Manages multiplayer color definitions and lists
- Handles starting money configurations
- Provides access to game timer, beacon limits, and shroud settings
- Supports random player templates, start positions, and colors

## Key Types
- **MultiplayerColorDefinition (Class)**: Stores color data (tooltip, RGB values, Color objects) for player teams.
- **MultiplayerColorList (Class)**: Typedef for a map of color definitions keyed by integer.
- **MultiplayerStartingMoneyList (Class)**: Typedef for a vector of Money values for starting money options.
- **MultiplayerSettings (Class)**: Main settings container with game rules, color management, and money configurations.

## Key Functions
### MultiplayerColorDefinition::setColor
- Purpose: Sets the day color for a team.
- Calls: None visible.

### MultiplayerColorDefinition::setNightColor
- Purpose: Sets the night color for a team.
- Calls: None visible.

### MultiplayerSettings::findMultiplayerColorDefinitionByName
- Purpose: Finds a color definition by name.
- Calls: None visible.

### MultiplayerSettings::newMultiplayerColorDefinition
- Purpose: Creates a new color definition.
- Calls: None visible.

### MultiplayerSettings::addStartingMoneyChoice
- Purpose: Adds a starting money option to the list.
- Calls: None visible.

## Globals
- **TheMultiplayerSettings (MultiplayerSettings*)**: Singleton instance of multiplayer settings.

## Dependencies
- `GameClient/Color.h` (Color, RGBColor)
- `Common/Money.h` (Money)
- `FieldParse` struct (forward-declared)
- `SubsystemInterface` (inheritance
