# Generals/Code/Tools/Babylon/DlgProxy.cpp

## Purpose
Implements the automation proxy class for the Noxstring dialog, enabling OLE automation support.

## Responsibilities
- Manages OLE automation lifecycle for the dialog
- Bridges between the dialog and automation clients
- Handles reference counting and object cleanup
- Exposes COM interfaces for external scripting

## Key Types
- CNoxstringDlgAutoProxy (Class): OLE automation proxy for the main dialog
- IID_INoxstring (IID): COM interface identifier for type-safe binding

## Key Functions
### CNoxstringDlgAutoProxy::CNoxstringDlgAutoProxy
- Purpose: Initializes the automation proxy and links it to the main dialog
- Calls: AfxOleLockApp, ASSERT

### CNoxstringDlgAutoProxy::OnFinalRelease
- Purpose: Cleans up when the last automation reference is released
- Calls: CCmdTarget::OnFinalRelease

## Globals
- IID_INoxstring (IID): GUID for the automation interface

## Dependencies
- "noxstring.h", "DlgProxy.h", "noxstringDlg.h"
- MFC classes: CCmdTarget, CWinApp
- OLE functions: AfxOleLockApp, AfxOleUnlockApp
- COM macros: IMPLEMENT_DYNCREATE, BEGIN_MESSAGE_MAP, BEGIN_DISPATCH_MAP, BEGIN_INTERFACE_MAP
