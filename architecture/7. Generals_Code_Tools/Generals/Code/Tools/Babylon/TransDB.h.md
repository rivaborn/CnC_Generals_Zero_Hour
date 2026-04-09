# Generals/Code/Tools/Babylon/TransDB.h

## Purpose
Header file defining translation database structures and classes for localization management in the game.

## Responsibilities
- Defines core translation database classes (TransDB, NoxLabel, NoxText, Translation)
- Provides language ID and reporting structures
- Declares wave file information tracking
- Manages string ID assignment and duplicate detection

## Key Types
- **TransDB (Class)**: Main translation database container
- **NoxLabel (Class)**: Container for labeled text groups
- **NoxText (Class)**: Individual translatable text string
- **Translation (Class)**: Language-specific translation of text
- **PMASK (Enum)**: Bitmask flags for translation error reporting
- **LangID (Enum)**: Language identifiers (US, UK, German, etc.)
- **LANGINFO (Struct)**: Language metadata container
- **CWaveInfo (Class)**: Wave file size and validity tracking
- **DLGREPORT/TRNREPORT (Struct)**: Translation quality reporting structures

## Key Functions
### FirstTransDB
- Purpose: Retrieves the first translation database in the system
- Calls: None

## Globals
- **START_STRING_ID (const int)**: Starting value for string ID assignment (10000)

## Dependencies
- "olestring.h", "list.h", "bin.h"
- CNoxstringDlg (forward declaration)
- OLEString, List, Bin, BinID (external types)
