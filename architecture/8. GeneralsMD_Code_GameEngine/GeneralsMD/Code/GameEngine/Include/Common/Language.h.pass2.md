# GeneralsMD/Code/GameEngine/Include/Common/Language.h - Enhanced Analysis

## Architectural Role
This header serves as the foundational language abstraction layer for the SAGE engine, providing language identifiers and wide-character string operations. It bridges the engine's internal string handling with the game's localization system, ensuring consistent language support across subsystems.

## Cross-References
### Incoming
- `GlobalLanguage` class (GameClient/GlobalLanguage.h) uses `LanguageID` for font size adjustments and parsing
- Likely used by UI, audio, and modding systems for localized content

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Macro Abstraction**: String operation macros hide platform-specific wide-character functions (e.g., `wcscpy` â `GameStrcpy`), enabling cross-platform compatibility.
- **Global State**: `OurLanguage` exposes current language as a global variable, used by subsystems for runtime localization.
- **Enum Consistency**: `LanguageID` mirrors the `Noxstring` tool's enum, ensuring toolchain alignment for localization pipelines.

*Not inferable*: No other patterns evident from header alone.
