# Generals/Code/Tools/Babylon/expimp.h - Enhanced Analysis

## Architectural Role
This header defines the core translation export/import interface for the Babylon localization tool, bridging the translation database (TransDB) with file I/O operations. It serves as the primary contract between the tool's UI and the underlying translation processing pipeline.

## Cross-References
### Incoming
- `Generals/Code/Tools/Babylon/expimp.cpp` (implementation)
- `Generals/Code/Tools/Babylon/main.cpp` (tool entry point)
- `Generals/Code/Tools/Babylon/transDB.cpp` (translation database operations)

### Outgoing
- `transDB.h` (translation database interface)
- `noxstringdlg.h` (progress dialog UI)

## Design Patterns
- **Strategy Pattern**: `TrFilter` and `GnFormat` enums encode different processing strategies for translations.
- **Facade Pattern**: The header exposes high-level operations (e.g., `ExportTranslations`) that hide complex file format handling.
- **Data Transfer Object (DTO)**: `TROPTIONS`, `GNOPTIONS`, and `RPOPTIONS` structs encapsulate configuration data for operations.
