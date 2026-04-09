# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwhack.h - Enhanced Analysis

## Architectural Role
This header provides a build-time mechanism to ensure critical library modules are linked into the final executable, addressing linker optimization that might otherwise exclude unused code. It's part of the build infrastructure rather than runtime logic.

## Cross-References
### Incoming
- Build system scripts (e.g., MSVC project files) likely use `DECLARE_FORCE_LINK` to mark modules
- Other WWDebug headers may include this for consistent linkage enforcement

### Outgoing
- None (pure header with macros only)

## Design Patterns
- **Macro-based Template Method**: The `FORCE_LINK` macro generates unique linker functions per module
- **Preprocessor Guard**: Standard include protection pattern
- **Build-time Hook**: Solves the "dead code elimination" problem common in large game engines

*Not inferable*: No runtime patterns observable in this header-only file.
