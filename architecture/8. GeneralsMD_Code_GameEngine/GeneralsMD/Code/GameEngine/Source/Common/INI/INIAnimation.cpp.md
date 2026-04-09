# GeneralsMD/Code/GameEngine/Source/Common/INI/INIAnimation.cpp

## Purpose
Parses animation definitions from INI files for 2D image animations in the game.

## Responsibilities
- Parses INI entries for 2D animations
- Manages animation template creation and lookup
- Handles INI initialization for animation objects
- Validates animation template uniqueness

## Key Types
- `INI` (Class): INI file parsing utility
- `Anim2DTemplate` (Class): Animation template data structure
- `TheAnim2DCollection` (Global): Collection of animation templates

## Key Functions
### `parseAnim2DDefinition`
- Purpose: Parses animation definitions from INI files
- Calls: `ini->getNextToken()`, `TheAnim2DCollection->findTemplate()`, `TheAnim2DCollection->newTemplate()`, `ini->initFromINI()`

## Globals
- `TheAnim2DCollection` (Anim2DCollection*): Global collection of animation templates

## Dependencies
- `PreRTS.h`
- `Common/INI.h`
- `GameClient/Anim2D.h`
- `AsciiString` class
- `DEBUG_ASSERTCRASH` and `DEBUG_CRASH` macros
