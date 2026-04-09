# Generals/Code/Tools/ParticleEditor/StdAfx.h - Enhanced Analysis

## Architectural Role
This precompiled header serves as the foundational include file for the ParticleEditor tool, centralizing common MFC and system headers to optimize build times. It isolates tool-specific build configurations from the main engine codebase.

## Cross-References
### Incoming
- ParticleEditor tool source files (e.g., main editor UI, particle system editors)

### Outgoing
- MFC core libraries (`afxwin.h`, `afxext.h`)
- Windows SDK headers (via MFC)
- Project-specific macros (IN/OUT, interface redefinition)

## Design Patterns
- **Precompiled Header Pattern**: Reduces build times by precompiling frequently used headers.
- **Header Guard Pattern**: Prevents multiple inclusions via unique macro (`AFX_STDAFX_H__FB15454D_21B4_4F33_A593_C13A58B86008__INCLUDED_`).
- **Macro Semantics Pattern**: Uses `IN`/`OUT` macros for parameter direction clarity (common in tooling but not in core engine).

**Note**: The `interface struct` redefinition suggests legacy compatibility with older compilers or codebases.
