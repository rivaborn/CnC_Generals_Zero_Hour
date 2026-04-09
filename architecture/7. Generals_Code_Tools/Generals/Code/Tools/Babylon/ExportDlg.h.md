# Generals/Code/Tools/Babylon/ExportDlg.h

## Purpose
Header file for a dialog class used to configure and initiate export operations in the Babylon tool.

## Responsibilities
- Manages user input for export settings (language, filename, options)
- Handles dialog initialization and data exchange
- Processes user selections and triggers export on confirmation

## Key Types
- CExportDlg (Class): Dialog class for export configuration
- (anonymous enum) (Enum): Contains IDD enum value
- IDD (Enum): Dialog resource identifier

## Key Functions
### CExportDlg::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### CExportDlg::OnOK
- Purpose: Processes export when user clicks OK
- Calls: Not inferable

### CExportDlg::OnInitDialog
- Purpose: Initializes dialog controls when dialog is created
- Calls: Not inferable

### CExportDlg::OnSelchangeCombolang
- Purpose: Handles language selection changes
- Calls: Not inferable

### CExportDlg::OnSelendokCombolang
- Purpose: Handles language selection completion
- Calls: Not inferable

## Globals
- None

## Dependencies
- "expimp.h" (included)
- CDialog, CWnd, CDataExchange (MFC classes)
- LangID, TROPTIONS (external types)
