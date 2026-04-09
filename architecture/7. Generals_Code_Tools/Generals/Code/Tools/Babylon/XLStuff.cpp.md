# Generals/Code/Tools/Babylon/XLStuff.cpp

## Purpose
This file provides an interface for interacting with Microsoft Excel via COM automation, allowing the tool to read/write Excel files.

## Responsibilities
- Excel application lifecycle management (open/close)
- Workbook operations (create/open/save/close)
- Cell data manipulation (read/write)
- Formatting operations (borders, sections, separators)

## Key Types
- None (primarily procedural with global state)

## Key Functions
### GetCell
- Purpose: Retrieves the value of a cell at specified row/column
- Calls: ws->GetRange, range->GetValue

### PutCell
- Purpose: Sets the value of a cell at specified row/column
- Calls: ws->GetRange, range->SetValue

### PutSeparator
- Purpose: Adds a horizontal separator line across a row
- Calls: ws->GetRange, borders->GetItem, border->SetLineStyle/ColorIndex/Weight

### PutSection
- Purpose: Creates a formatted section header with borders and background
- Calls: ws->GetRange, borders->GetItem, border->SetLineStyle/ColorIndex/Weight, interior->SetColorIndex/Pattern

### OpenExcel
- Purpose: Initializes Excel COM automation and creates application instance
- Calls: _Application::CreateDispatch, xl->GetWorkbooks

### CloseExcel
- Purpose: Cleans up Excel resources and closes application
- Calls: CloseWorkBook, xl->Quit, xl->ReleaseDispatch

### OpenWorkBook
- Purpose: Opens an existing Excel workbook
- Calls: wbs->Open, SelectActiveSheet

### NewWorkBook
- Purpose: Creates a new Excel workbook
- Calls: wbs->Add, SelectActiveSheet

### SaveWorkBook
- Purpose: Saves the current workbook
- Calls: workbook->SaveAs, ws->Protect

### SelectActiveSheet
- Purpose: Selects the active sheet in the workbook
- Calls: xl->GetActiveSheet, ws->AttachDispatch

### GetInt
- Purpose: Retrieves an integer value from a cell
- Calls: GetCell

### GetString
- Purpose: Retrieves a string value from a cell
- Calls: GetCell

## Globals
- xlWorkbookNormal (int): Excel workbook format constant
- xlNoChange (int): Excel save changes constant
- xlLocalSessionChanges (int): Excel session changes constant
- xlWBATWorksheet (int): Excel worksheet type constant
- workbook (_Workbook*): Current workbook reference
- xl (_Application*): Excel application instance
- wbs (Workbooks*): Workbooks collection
- range (Range*): Current range reference
- ws (_Worksheet*): Current worksheet
- buffer (OLECHAR[]): Temporary buffer for string operations
- no/yes/dummy/dummy0/nullstring/empty (VARIANT): Pre-initialized COM variants
- continuous/automatic/medium/thin/none/solid/yellow (VARIANT): Pre-initialized formatting variants

## Dependencies
- stdAfx.h, noxstring.h, resource.h, xlstuff.h, comdef.h
- COM automation interfaces (_Application, _Workbook, _Worksheet, Range, Borders, Border, Interior)
- Windows API (FindFirstFile, FindClose)
