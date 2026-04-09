# Generals/Code/Tools/Babylon/expimp.h

## Purpose
Header file for translation export/import functionality in the Babylon tool.

## Responsibilities
- Defines data structures for translation export/import options
- Declares core translation processing functions
- Specifies file format constants for translation files

## Key Types
- TrFilter (Enum): translation filtering criteria
- TROPTIONS (Struct): options for translation export
- GnFormat (Enum): output file format options
- GnUntranslated (Enum): handling of untranslated text
- GNOPTIONS (Struct): options for game file generation
- RPOPTIONS (Struct): options for report generation
- CSF_HEADER_V1/CSF_HEADER (Struct): translation file header formats

## Key Functions
### ExportTranslations
- Purpose: Exports translations to a file
- Calls: None visible

### ImportTranslations
- Purpose: Imports translations from a file
- Calls: None visible

### UpdateSentTranslations
- Purpose: Updates sent translations
- Calls: None visible

### GenerateGameFiles
- Purpose: Generates game files from translations
- Calls: None visible

### GenerateReport
- Purpose: Generates a report of translations
- Calls: None visible

### ProcessWaves
- Purpose: Processes wave files for translations
- Calls: None visible

## Globals
- CSF_ID, CSF_LABEL, CSF_STRING, CSF_STRINGWITHWAVE, CSF_VERSION (Macros): file format identifiers

## Dependencies
- transDB.h: translation database interface
- noxstringdlg.h: UI dialog for progress reporting
