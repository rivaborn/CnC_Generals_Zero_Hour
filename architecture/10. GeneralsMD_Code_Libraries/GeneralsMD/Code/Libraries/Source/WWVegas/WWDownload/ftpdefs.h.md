# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/ftpdefs.h

## Purpose
Defines FTP operation return codes for the game's download functionality.

## Responsibilities
- Defines standard FTP success/failure return codes
- Provides a "trying" state code for async operations
- Uses Windows HRESULT conventions for error reporting

## Key Types
None

## Key Functions
None

## Globals
- FTP_SUCCEEDED (S_OK): Success status code
- FTP_FAILED (HRESULT): Generic failure status code
- FTP_TRYING (HRESULT): Operation in progress status code

## Dependencies
- Windows HRESULT macros (MAKE_HRESULT, SEVERITY_ERROR, FACILITY_ITF)
- S_OK from Windows headers
