# Generals/Code/Tools/Babylon/XLStuff.h

## Purpose
Header file defining constants and functions for Excel automation in the Babylon tool.

## Responsibilities
- Defines Excel-related enums for formatting, borders, and cell types
- Declares functions for Excel workbook manipulation
- Provides cell data input/output functions

## Key Types
- Constants (Enum): Excel formatting and option constants
- XlBorderWeight (Enum): Border line weight options
- XlLineStyle (Enum): Line style options for borders
- XlBordersIndex (Enum): Border position indices
- CELL_* (Enum): Cell content type identifiers

## Key Functions
### OpenExcel
- Purpose: Initialize Excel automation
- Calls: Not inferable

### NewWorkBook
- Purpose: Create a new Excel workbook
- Calls: Not inferable

### PutCell
- Purpose: Write data to a specific cell
- Calls: Not inferable

### GetInt
- Purpose: Read integer value from a cell
- Calls: Not inferable

### GetString
- Purpose: Read string value from a cell
- Calls: Not inferable

## Globals
- ROW_COUNT (int): Row count constant
- COLUMN_COUNT (int): Column count constant
- ROW_LANGUAGE (int): Language row constant
- COLUMN_LANGUAGE (int): Language column constant

## Dependencies
- "noxstringDlg.h" header
- OLECHAR type (Windows COM)
- Boolean constants (FALSE)
