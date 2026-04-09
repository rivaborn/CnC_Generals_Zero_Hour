# Generals/Code/Tools/WorldBuilder/src/ExportScriptsOptions.cpp

## Purpose
Implements a dialog for configuring script export options in WorldBuilder.

## Responsibilities
- Manages checkbox states for script export options
- Handles dialog initialization and validation
- Stores export preferences as static member variables

## Key Types
- ExportScriptsOptions (Class): Dialog class for script export options

## Key Functions
### ExportScriptsOptions::OnOK
- Purpose: Saves checkbox states to static member variables
- Calls: GetDlgItem, CButton::GetCheck, CDialog::OnOK

### ExportScriptsOptions::OnInitDialog
- Purpose: Initializes checkbox states from static member variables
- Calls: GetDlgItem, CButton::SetCheck, CDialog::OnInitDialog

## Globals
- m_units (Bool): Controls whether units are exported
- m_waypoints (Bool): Controls whether waypoints are exported
- m_triggers (Bool): Controls whether triggers are exported
- m_allScripts (Bool): Controls whether all scripts are exported

## Dependencies
- stdafx.h, worldbuilder.h, ExportScriptsOptions.h
- MFC classes: CDialog, CButton, CDataExchange
- Message map macros: BEGIN_MESSAGE_MAP, END_MESSAGE_MAP
