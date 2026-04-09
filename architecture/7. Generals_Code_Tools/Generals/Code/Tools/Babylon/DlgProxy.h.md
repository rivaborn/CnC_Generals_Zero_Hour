# Generals/Code/Tools/Babylon/DlgProxy.h

## Purpose
Header file defining an OLE automation proxy class for a dialog.

## Responsibilities
- Provides OLE automation support for `CNoxstringDlg`
- Manages dialog instance via `m_pDialog` pointer
- Implements `CCmdTarget` for COM command routing
- Declares message and dispatch maps for MFC/COM integration

## Key Types
- **CNoxstringDlg (Class)**: Forward-declared dialog class this proxy serves.
- **CNoxstringDlgAutoProxy (Class)**: OLE automation proxy for `CNoxstringDlg`; inherits from `CCmdTarget`.

## Key Functions
### OnFinalRelease
- Purpose: Called when the last reference to the object is released.
- Calls: Not inferable (implementation in .cpp).

### ~CNoxstringDlgAutoProxy
- Purpose: Destructor for the proxy class.
- Calls: Not inferable (implementation in .cpp).

### DECLARE_MESSAGE_MAP / DECLARE_DISPATCH_MAP / DECLARE_INTERFACE_MAP
- Purpose: MFC/COM macro declarations for message routing and OLE dispatch.
- Calls: Not inferable (expanded by preprocessor).

## Globals
- None

## Dependencies
- `CCmdTarget` (MFC base class)
- MFC/COM macros (`DECLARE_DYNCREATE`, `DECLARE_MESSAGE_MAP`, etc.)
- `CNoxstringDlg` (forward-declared)
