# GeneralsMD/Code/GameEngine/Include/GameClient/Credits.h

## Purpose
Header file for the credits system in the game.

## Responsibilities
- Defines credit line styles and parsing logic
- Manages scrolling credits display
- Handles initialization, loading, and rendering of credits
- Provides interface for adding text and blank lines to credits

## Key Types
- **CreditsLine (Class)**: Represents a single line in the credits with text and display properties
- **CreditsManager (Class)**: Manages the credits system, including parsing, scrolling, and rendering
- **CREDIT_STYLE_* (Enum)**: Defines different credit line styles (TITLE, POSITION, NORMAL, COLUMN, BLANK)
- **DisplayString (Class)**: Forward reference to display string handling (external)

## Key Functions
### CreditsManager::parseBlank
- Purpose: Parses blank credit lines from INI files
- Calls: Not inferable (static method)

### CreditsManager::parseText
- Purpose: Parses text credit lines from INI files
- Calls: Not inferable (static method)

### CreditsManager::getUnicodeString
- Purpose: Converts ASCII strings to Unicode strings for display
- Calls: Not inferable

## Globals
- **TheCredits (CreditsManager*)**: Global instance of the credits manager
- **CreditStyleNames (LookupListRec[])**: Mapping of credit style names to enum values

## Dependencies
- `GameClient/FontDesc.h`
- `DisplayString` class (forward reference)
- `INI` class for parsing
- `SubsystemInterface` base class
- Standard C++ list container
