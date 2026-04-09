# Generals/Code/Tools/buildVersionUpdate/buildVersionUpdate.cpp

## Purpose
This file is a utility program that updates version numbers in a header file for the Command & Conquer Generals build system.

## Responsibilities
- Parses command-line arguments to identify the target header file.
- Reads the current version numbers from the header file.
- Increments the build number and writes updated version definitions back to the file.
- Provides usage instructions if arguments are invalid.

## Key Types
- None

## Key Functions
### writeVersion
- Purpose: Writes version definitions to a specified file.
- Calls: `fopen`, `fprintf`, `fclose`

### usage
- Purpose: Prints usage instructions for the program.
- Calls: `printf`

### strtrim
- Purpose: Trims leading and trailing whitespace from a string in-place.
- Calls: `strlen`, `strcpy`, `strtok`

### WinMain
- Purpose: Entry point that parses arguments, reads the version file, increments the build number, and writes updates.
- Calls: `strtok`, `fopen`, `fread`, `strstr`, `strtok`, `atoi`, `writeVersion`, `printf`

## Globals
- `VERSION_MAJOR` (const char*): String literal for major version define.
- `VERSION_MINOR` (const char*): String literal for minor version define.
- `VERSION_BUILDNUM` (const char*): String literal for build number define.
- `VERSION_STRING` (const char*): String literal for version string define.
- `FORMAT` (const char*): Format string for version define.
- `COMMENTS` (const char*): Comment header for generated file.
- `NUMFMT` (const char*): Format string for numeric defines.
- `NUMFMT_MINOR` (const char*): Format string for minor version define with
