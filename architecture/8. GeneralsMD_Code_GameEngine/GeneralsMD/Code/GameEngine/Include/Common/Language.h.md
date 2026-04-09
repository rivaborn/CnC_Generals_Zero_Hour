# GeneralsMD/Code/GameEngine/Include/Common/Language.h

## Purpose
Defines language identifiers and string manipulation macros for the game.

## Responsibilities
- Declares `LanguageID` enum for supported languages
- Provides wide-character string operation macros
- Exposes global `OurLanguage` variable

## Key Types
- LanguageID (Enum): language identifiers (US, UK, German, etc.)
- (anonymous enum): same as LanguageID (lines 62-76)

## Key Functions
None (header-only file with macros and declarations)

## Globals
- OurLanguage (LanguageID): tracks current language setting

## Dependencies
- None (header-only, no external symbols)
