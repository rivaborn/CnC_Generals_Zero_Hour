# Generals/Code/GameEngine/Source/GameClient/Credits.cpp

## Purpose
Manages the display of scrolling credits in the game, loading from INI files and rendering text with different styles.

## Responsibilities
- Loads and parses credit text from INI files
- Manages scrolling behavior (direction, speed)
- Handles different credit styles (titles, positions, normal text, columns)
- Updates and renders credit lines
- Cleans up display strings and credit lines

## Key Types
- **CreditsManager (Class)**: Main class handling credits logic
- **CreditsLine (Class)**: Represents a single line of credit text
- **CreditsLineList (Type)**: List of CreditsLine objects
- **CreditStyle (Enum)**: Defines credit text styles (title, position, normal, column, blank)

## Key Functions
### `CreditsManager::update`
- Purpose: Updates credit positions and adds new lines when needed
- Calls: `TheDisplayStringManager->freeDisplayString`, `TheDisplay->getHeight`

### `CreditsManager::draw`
- Purpose: Renders all visible credit lines with appropriate colors and positions
- Calls: `TheDisplay->getHeight`, `TheDisplay->getWidth`, `DisplayString::draw`

### `CreditsManager::addText`
- Purpose: Adds a new text line to the credits
- Calls: `getUnicodeString`

### `CreditsManager::parseText`
- Purpose: INI parser callback for text entries
- Calls: `addText`

## Globals
- **TheCredits (CreditsManager*)**: Global instance of the credits manager

## Dependencies
- `INI.h`, `Credits.h`, `DisplayStringManager.h`, `Display.h`, `GameText.h`, `GlobalLanguage.h`
- `TheDisplayStringManager`, `TheDisplay`, `TheFontLibrary`, `TheGlobalLanguageData`, `TheGameText`
