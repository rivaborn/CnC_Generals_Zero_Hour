# Generals/Code/Tools/WorldBuilder/include/StdAfx.h - Enhanced Analysis

## Architectural Role
This precompiled header serves as the foundational include file for the WorldBuilder tool, a level-editing utility in the Generals toolchain. It centralizes common system and project headers to optimize build times, particularly for MFC-based tooling.

## Cross-References
### Incoming
- Likely included by all WorldBuilder tool source files (e.g., `WorldBuilder.cpp`, `TerrainEditor.cpp`)

### Outgoing
- Pulls in MFC core components (`afxwin.h`, `afxext.h`) and project-specific headers (`Basetype.h`)

## Design Patterns
- **Precompiled Header Pattern**: Reduces build times by precompiling frequently used headers
- **Header Guard Pattern**: Uses `#ifndef` to prevent multiple inclusions
- **Conditional Compilation**: Uses `#ifndef _AFX_NO_AFXCMN_SUPPORT` for optional MFC components

*Not inferable*: No other patterns evident from this file alone.
