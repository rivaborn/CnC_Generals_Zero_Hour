# Generals/Code/Tools/wolSetup/WOLAPI/ftpdefs.h - Enhanced Analysis

## Architectural Role
This header defines the error handling conventions for FTP operations within the WOL (Westwood Online) API tooling layer. It serves as a contract for FTP-related error codes used across the WOL setup utilities.

## Cross-References
### Incoming
- Likely referenced by FTP client implementations in the WOL setup tools (e.g., `Generals/Code/Tools/wolSetup/WOLAPI/ftp.cpp`)

### Outgoing
- None (pure header with no external dependencies beyond Windows HRESULT macros)

## Design Patterns
- **Error Code Enumeration**: Uses Windows HRESULT pattern for cross-platform compatibility
- **Header Guard**: Standard include protection pattern
- **Constant Abstraction**: Wraps raw HRESULT values in semantic constants

Not inferable: No visible usage patterns or relationships to other subsystems.
