# Generals/Code/Tools/wolSetup/WOLAPI/netutildefs.h

## Purpose
Defines error and success codes for network utility functions in the WOL (Westwood Online) API.

## Responsibilities
- Defines HRESULT-based error codes for network operations.
- Defines a success status code.
- Uses MAKE_HRESULT macro to construct standard COM-style error codes.

## Key Types
None

## Key Functions
None

## Globals
- NETUTIL_E_ERROR (HRESULT): Generic error code.
- NETUTIL_E_BUSY (HRESULT): Resource busy error code.
- NETUTIL_E_TIMEOUT (HRESULT): Operation timeout error code.
- NETUTIL_E_INVALIDFIELD (HRESULT): Invalid field data error code.
- NETUTIL_E_CANTVERIFY (HRESULT): Verification failure error code.
- NETUTIL_S_FINISHED (HRESULT): Operation completed successfully.

## Dependencies
- MAKE_HRESULT macro (assumed from Windows SDK)
- SEVERITY_ERROR, SEVERITY_SUCCESS, FACILITY_ITF (Windows HRESULT constants)
