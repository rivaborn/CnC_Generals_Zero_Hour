# Generals/Code/Tools/ParticleEditor/StdAfx.h

## Purpose
Precompiled header file for the ParticleEditor tool, including standard system and MFC headers.

## Responsibilities
- Includes common system and MFC headers
- Defines project-specific macros (IN, OUT, interface)
- Disables specific compiler warnings
- Prevents multiple inclusions via header guard

## Key Types
None

## Key Functions
None

## Globals
None

## Dependencies
- `<afxwin.h>`: MFC core components
- `<afxext.h>`: MFC extensions
- `<afxole.h>`: MFC OLE classes (conditional)
- `<afxodlgs.h>`: MFC OLE dialog classes (conditional)
- `<afxdisp.h>`: MFC Automation classes (conditional)
- `<afxdb.h>`: MFC ODBC database classes (conditional)
- `<afxdao.h>`: MFC DAO database classes (conditional)
- `<afxdtctl.h>`: MFC support for IE4 Common Controls
- `<afxcmn.h>`: MFC support for Windows Common Controls (conditional)
