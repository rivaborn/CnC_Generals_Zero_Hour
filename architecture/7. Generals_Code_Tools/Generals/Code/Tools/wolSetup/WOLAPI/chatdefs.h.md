# Generals/Code/Tools/wolSetup/WOLAPI/chatdefs.h

## Purpose
Defines error codes, success codes, and bit flags for the Westwood Online (WOL) chat API.

## Responsibilities
- Defines version constants for the chat API
- Declares error and success HRESULT codes for chat operations
- Defines bit flags for user and channel attributes

## Key Types
None

## Key Functions
None

## Globals
- `CHAT_VERSION_MAJOR` (int): Major version number (1)
- `CHAT_VERSION_MINOR` (int): Minor version number (16)
- `CHAT_VERSION` (int): Combined version number

## Dependencies
- `MAKE_HRESULT`: Macro for creating HRESULT values
- `SEVERITY_ERROR`, `SEVERITY_SUCCESS`: Severity constants
- `FACILITY_ITF`: Facility constant
