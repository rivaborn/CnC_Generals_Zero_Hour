# Generals/Code/Tools/WW3D/max2w3d/FormClass.h

## Purpose
Defines a base class for creating and managing dialog forms in the max2w3d tool.

## Responsibilities
- Provides a framework for creating and displaying dialog forms
- Manages the Windows handle for the dialog
- Handles dialog message processing
- Supports dialog initialization and invalidation

## Key Types
- FormClass (Class): Base class for dialog forms in max2w3d tool

## Key Functions
### FormClass::Create_Form
- Purpose: Creates the dialog form window
- Calls: Not inferable

### FormClass::Dialog_Proc
- Purpose: Pure virtual function for handling dialog messages
- Calls: Not inferable

### FormClass::ExecuteDlgInit
- Purpose: Initializes the dialog from resources
- Calls: Not inferable

### FormClass::fnFormProc
- Purpose: Static callback function for dialog procedures
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<Max.h>` (3ds Max SDK)
- `ParamDlg` (base class from 3ds Max SDK)
- Windows API types (`HWND`, `UINT`, `WPARAM`, `LPARAM`, `RECT`, `LPTSTR`, `LPCTSTR`)
