# Generals/Code/Tools/WorldBuilder/src/propedit.cpp

## Purpose
Implements a dialog for editing dictionary properties (key-value pairs) in WorldBuilder.

## Responsibilities
- Manages UI controls for key, type, and value editing
- Validates input based on data type rules
- Updates underlying data structures when changes occur
- Handles boolean, integer, real, and string property types

## Key Types
- PropEdit (Class): Dialog for editing dictionary properties
- Dict::DataType (Enum): Represents property data types (bool, int, real, string)

## Key Functions
### PropEdit::validate
- Purpose: Validates and updates property values and UI state
- Calls: GetDlgItem, GetCurSel, GetWindowText, SetWindowText, GetCheck

### PropEdit::OnInitDialog
- Purpose: Initializes dialog controls with current property values
- Calls: CDialog::OnInitDialog, GetDlgItem, SetCurSel, SetWindowText, SetCheck, validate

### PropEdit::OnChangeKeyname / OnEditchangeKeytype / OnCloseupKeytype / OnSelchangeKeytype / OnChangeValue / OnPropbool
- Purpose: Event handlers that trigger validation on UI changes
- Calls: validate

## Globals
- None

## Dependencies
- "stdafx.h", "worldbuilder.h", "..\include\propedit.h"
- CDialog, CWnd, CComboBox, CButton, CString, AsciiString, Dict::DataType
- MFC message map macros (BEGIN_MESSAGE_MAP, ON_EN_CHANGE, etc.)
