# Generals/Code/Tools/Autorun/Locale_API.cpp - Enhanced Analysis

## Architectural Role
This file serves as the localization bridge for the autorun tool, abstracting language-specific string handling. It interfaces with both legacy LOCALE_ functions and the modern GameText system, enabling fallback mechanisms for missing translations.

## Cross-References
### Incoming
- Likely called by autorun UI components needing localized text
- Potentially referenced by build scripts or installer logic

### Outgoing
- Calls into `GameText.h` interface for string management
- Uses `LOCALE_*` functions for legacy language file support
- Depends on Windows API (`WideCharToMultiByte`, `GetACP`) for encoding conversion

## Design Patterns
- **Adapter Pattern**: Wraps legacy `LOCALE_*` functions and modern `GameText` interface behind a unified API
- **Fallback Strategy**: Uses `localeStringsMissing` array when translations are unavailable
- **Resource Management**: Explicit cleanup in `Locale_Restore` for both single/multi-file formats

*Not inferable*: Exact caller relationships or multi-file format usage context.
