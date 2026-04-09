# Generals/Code/Tools/versionUpdate/versionUpdate.cpp

## Purpose
This file is a Windows tool that updates version information in a header file, incrementing the build number and recording the username and computer name.

## Responsibilities
- Parse command-line arguments to identify the target header file.
- Read and increment the build number from the header file.
- Write updated version information (build number, username, computer name) to the header file.
- Display usage instructions if arguments are invalid.

## Key Types
- None

## Key Functions
### writeVersion
- Purpose: Writes version information (build number, username, computer name) to the specified file.
- Calls: `fopen`, `fprintf`, `fclose`, `GetUserName`, `GetComputerName`, `strcpy`

### usage
- Purpose: Prints the usage instructions for the tool.
- Calls: `printf`

### strtrim
- Purpose: Trims leading and trailing whitespace from a string in place.
- Calls: `strcpy`, `strlen`

### WinMain
- Purpose: Entry point for the Windows application, parses arguments, reads the build number, increments it, and writes the updated version information.
- Calls: `strtok`, `strtrim`, `fopen`, `fread`, `strstr`, `strtok`, `atoi`, `fclose`, `writeVersion`, `usage`, `printf`

## Globals
- `VERSION_BUILDNUM` (String): Define key for build number.
- `VERSION_STRING` (String): Define key for build string.
- `VERSION_BUILDUSER` (String): Define key for build user.
- `VERSION_BUILDLOC` (String): Define key for build location.
- `FORMAT` (String): Format string for build number.
- `COMMENTS` (String): Comment header for generated file.
- `NUMFMT` (String): Format string for numeric defines.
- `STRFMT` (String): Format string for string defines.

## Dependencies
- Windows API: `GetUserName`, `GetComputerName`
- C Runtime: `fopen`, `fprintf`, `fclose`, `printf`, `strcpy`, `strlen`, `strstr`, `strtok`, `atoi`, `fread`, `feof`
- Custom: None
