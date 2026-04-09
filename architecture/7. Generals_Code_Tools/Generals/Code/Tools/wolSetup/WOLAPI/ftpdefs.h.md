# Generals/Code/Tools/wolSetup/WOLAPI/ftpdefs.h

## Purpose
Defines FTP return codes for the WOL (Westwood Online) API.

## Responsibilities
- Defines FTP operation success/failure/error codes
- Uses Windows HRESULT macros for error handling
- Provides constants for FTP operation states

## Key Types
None

## Key Functions
None

## Globals
- FTP_SUCCEEDED (S_OK): Success status code
- FTP_FAILED (HRESULT): Generic failure code
- FTP_TRYING (HRESULT): Operation in progress code

## Dependencies
- Windows HRESULT macros (S_OK, MAKE_HRESULT, SEVERITY_ERROR, FACILITY_ITF)
