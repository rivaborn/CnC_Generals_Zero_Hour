# Generals/Code/Tools/WorldBuilder/src/BaseBuildProps.cpp

## Purpose
Implements a dialog for editing base building properties in WorldBuilder.

## Responsibilities
- Displays and edits name, script, health, and unsellable flag for map objects.
- Initializes dialog controls with current property values.
- Updates property values when dialog is closed.

## Key Types
- **BaseBuildProps (class)**: Dialog for editing base building properties.

## Key Functions
### `BaseBuildProps::BaseBuildProps`
- Purpose: Constructor for the dialog.
- Calls: None.

### `BaseBuildProps::DoDataExchange`
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: `CDialog::DoDataExchange`.

### `BaseBuildProps::OnInitDialog`
- Purpose: Initializes dialog controls with current property values.
- Calls: `GetDlgItem`, `SetWindowText`, `EditParameter::loadScripts`, `SelectString`.

### `BaseBuildProps::setProps`
- Purpose: Sets the property values for the dialog.
- Calls: None.

### `BaseBuildProps::OnOK`
- Purpose: Updates property values from dialog controls when OK is clicked.
- Calls: `GetDlgItem`, `GetWindowText`, `atoi`, `GetCheck`, `CDialog::OnOK`.

## Globals
- None.

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `BaseBuildProps.h`, `EditParameter.h`
- `CDialog`, `CWnd`, `CComboBox`, `CButton`, `CString`, `AsciiString`, `Int`, `Bool`
