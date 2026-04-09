# GeneralsMD/Code/GameEngine/Source/GameClient/Credits.cpp

## Purpose
Manages the display and scrolling of credits text in the game.

## Responsibilities
- Loads and parses credits data from INI files
- Manages scrolling behavior (direction, speed) for credits text
- Handles rendering of different credit styles (titles, positions, normal text, columns)
- Tracks displayed credits and updates their positions over time

## Key Types
- **CreditsManager (Class)**: Main class handling credits logic, loading, updating, and drawing
- **CreditsLine (Class)**: Represents a single line of credits text with position, style, and display properties
- **CreditsLineList (Type)**: Container for managing multiple credits lines
- **CreditStyle (Enum)**: Defines different credit text styles (title, position, normal, column, blank)

## Key Functions
### `update`
- Purpose: Updates the positions of credits lines and manages scrolling behavior
- Calls: `TheDisplayStringManager->freeDisplayString`, `TheDisplay->getHeight`, `TheDisplay->getWidth`

### `draw`
- Purpose: Renders all currently displayed credits lines with appropriate styling and fade effects
- Calls: `TheDisplay->getHeight`, `TheDisplay->getWidth`, `DisplayString::draw`

### `addText`
- Purpose: Adds a new text entry to the credits list based on current style settings
- Calls: `getUnicodeString`

### `parseText`
- Purpose: INI parsing callback for adding text entries
- Calls: `addText`

## Globals
- **TheCredits (CreditsManager*)**: Global instance of the credits manager

## Dependencies
- Key includes: `PreRTS.h`, `Common/INI.h`, `GameClient/Credits.h`, `GameClient/DisplayStringManager.h`, `GameClient/Display.h`, `GameClient/GameText.h`, `GameClient/GlobalLanguage.h`
- External symbols: `TheDisplayStringManager`, `TheDisplay`, `TheFontLibrary`, `TheGlobalLanguageData`, `TheGameText`
