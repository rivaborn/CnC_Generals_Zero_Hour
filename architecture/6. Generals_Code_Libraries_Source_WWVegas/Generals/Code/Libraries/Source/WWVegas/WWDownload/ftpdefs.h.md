# Generals/Code/Libraries/Source/WWVegas/WWDownload/ftpdefs.h

## Purpose
Defines FTP operation return codes for the game's download functionality.

## Responsibilities
- Defines standard FTP success/failure return codes.
- Provides a "trying" state code for async operations.
- Uses Windows HRESULT conventions for error reporting.

## Key Types
None

## Key Functions
None

## Globals
- `FTP_SUCCEEDED` (macro): Success status code (S_OK).
- `FTP_FAILED` (macro): Generic failure status code.
- `FTP_TRYING` (macro): In-progress status code.

## Dependencies
- Windows HRESULT macros (`S_OK`, `MAKE_HRESULT`, `SEVERITY_ERROR`, `FACILITY_ITF`).
