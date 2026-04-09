# Generals/Code/Tools/wolSetup/wolSetup.h

## Purpose
Header file for Windows Online (WOL) setup utilities in Command & Conquer Generals.

## Responsibilities
- Declares functions for checking WOL API version and setting up Generals.
- Defines global variables for WOL API and Generals installation state.
- Provides macros for extracting major/minor version numbers.

## Key Types
None

## Key Functions
### checkInstalledWolapiVersion
- Purpose: Checks the installed version of the WOL API.
- Calls: None

### setupGenerals
- Purpose: Sets up Generals installation with given path and serial.
- Calls: None

### MAJOR
- Purpose: Extracts major version number from a version value.
- Calls: None

### MINOR
- Purpose: Extracts minor version number from a version value.
- Calls: None

## Globals
- g_hInst (HINSTANCE): Stores the instance handle for the application.
- g_wolapiRegistryVersion (unsigned long): Stores the WOL API version from the registry.
- g_wolapiRealVersion (unsigned long): Stores the actual WOL API version.
- g_wolapiInstalled (bool): Indicates whether WOL API is installed.
- g_wolapiRegFilename (char[MAX_PATH]): Path to the WOL API registry file.
- g_wolapi
