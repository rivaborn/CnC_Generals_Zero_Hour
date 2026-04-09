# Generals/Code/Tools/Babylon/MatchDlg.cpp

## Purpose
Handles the UI dialog for resolving unmatched text strings in the Babylon localization tool.

## Responsibilities
- Displays unmatched text strings for user selection
- Manages matching/unmatching of text entries
- Provides options to skip or cancel text resolution
- Updates retranslation flags for matched text

## Key Types
- **CMatchDlg (Class)**: Dialog class for text matching UI
- **NoxText (Type)**: Represents a text string in the localization system
- **NoxLabel (Type)**: Container for multiple text strings
- **ListSearch (Type)**: Iterator for traversing text lists

## Key Functions
### OnMatch
- Purpose: Applies the selected text match and sets retranslation flag
- Calls: `GetDlgItem`, `CButton::GetCheck`, `NoxText::SetRetranslate`

### OnInitDialog
- Purpose: Initializes the dialog with unmatched text options
- Calls: `SetWindowText`, `GetDlgItem`, `CComboBox::InsertString`, `CComboBox::SetItemDataPtr`, `NoxLabel::FirstText`, `NoxLabel::NextText`

### OnSelchangeMatchcombo
- Purpose: Updates preview when combo box selection changes
- Calls: `GetDlgItem`, `CComboBox::GetCurSel`, `CComboBox::GetItemDataPtr`, `CStatic::SetWindowText`

## Globals
- **MatchingNoxText (NoxText*)**: Currently selected text for matching
- **MatchOriginalText (NoxText*)**: Original unmatched text being resolved
- **MatchLabel (NoxLabel*)**: Container holding text strings
- **current_match (NoxText*)**: Temporary pointer to selected match candidate

## Dependencies
- MFC dialog framework (`CDialog
