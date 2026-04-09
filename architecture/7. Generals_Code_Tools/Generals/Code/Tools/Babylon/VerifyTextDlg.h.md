# Generals/Code/Tools/Babylon/VerifyTextDlg.h

## Purpose
Header file for a dialog class used to verify text translations in the Babylon tool.

## Responsibilities
- Define the `CVerifyTextDlg` class for text verification.
- Declare dialog data and message handlers.
- Manage translation and original text strings.

## Key Types
- **CVerifyTextDlg (Class)**: Dialog for comparing translated and original text.
- **(anonymous enum) (Enum)**: Contains `IDD` enum value.
- **IDD (Enum)**: Dialog resource ID.

## Key Functions
### CVerifyTextDlg::CVerifyTextDlg
- Purpose: Constructor for the dialog.
- Calls: None.

### CVerifyTextDlg::DoDataExchange
- Purpose: Handles data exchange between controls and member variables.
- Calls: None.

### CVerifyTextDlg::OnNomatch
- Purpose: Handles the "No Match" button click.
- Calls: None.

### CVerifyTextDlg::OnMatch
- Purpose: Handles the "Match" button click.
- Calls: None.

### CVerifyTextDlg::OnInitDialog
- Purpose: Initializes the dialog.
- Calls: None.

## Globals
- **m_trans (char*)**: Stores the translated text.
- **m_orig (char*)**: Stores the original text.

## Dependencies
- `CDialog`, `CWnd`, `CDataExchange` (MFC classes).
- `DECLARE_MESSAGE_MAP()` (MFC macro).
