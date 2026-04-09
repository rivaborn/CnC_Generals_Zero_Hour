# Generals/Code/Tools/DebugWindow/StdAfx.h

## Purpose
Precompiled header file for the DebugWindow tool, including standard system and MFC headers.

## Responsibilities
- Includes common MFC headers (afxwin.h, afxext.h, etc.)
- Disables specific compiler warnings
- Defines include guards
- Conditionally includes OLE, database, and common control headers

## Key Types
None

## Key Functions
None

## Globals
None

## Dependencies
- MFC headers (afxwin.h, afxext.h, afxole.h, afxodlgs.h, afxdisp.h, afxdb.h, afxdao.h, afxdtctl.h, afxcmn.h)
- Windows SDK headers (via MFC includes)
- Compiler-specific pragmas (_MSC_VER)
