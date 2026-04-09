# Generals/Code/Tools/Babylon/MatchDlg.h

## Purpose
Header file for a dialog class handling matchmaking functionality in the Babylon tool.

## Responsibilities
- Defines the `CMatchDlg` dialog class for matchmaking UI
- Declares event handlers for matchmaking actions
- Manages NoxText and NoxLabel UI elements for match status

## Key Types
- CMatchDlg (Class): Dialog for matchmaking UI and logic
- (anonymous enum) (Enum): Contains IDD_MATCH dialog identifier
- IDD (Enum): Dialog resource identifier

## Key Functions
### CMatchDlg::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### CMatchDlg::OnCancel
- Purpose: Handles dialog cancellation
- Calls: Not inferable

### CMatchDlg::OnNomatch
- Purpose: Handles no-match scenario
- Calls: Not inferable

### CMatchDlg::OnMatch
- Purpose: Handles successful match
- Calls: Not inferable

### CMatchDlg::OnInitDialog
- Purpose: Initializes dialog controls
- Calls: Not inferable

### CMatchDlg::OnSkip
- Purpose: Handles skip action
- Calls: Not inferable

### CMatchDlg::OnSelchangeMatchcombo
- Purpose: Handles match combo selection change
- Calls: Not inferable

## Globals
- MatchingNoxText (NoxText*): UI element for match status
- MatchOriginalText (NoxText*): Original match text
- MatchLabel (NoxLabel*): Label for match UI

## Dependencies
- "transDB.h" for translation database
- CDialog, CWnd, CDataExchange from MFC
- NoxText, NoxLabel (custom UI classes)
