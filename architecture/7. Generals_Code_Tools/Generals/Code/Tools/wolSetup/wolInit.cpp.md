# Generals/Code/Tools/wolSetup/wolInit.cpp

## Purpose
Initializes and manages Westwood Online (WOL) API and COM/OLE infrastructure for Generals setup.

## Responsibilities
- Initializes COM/OLE for WOLAPI
- Reads/writes Generals/WOLAPI paths and versions from Windows registry
- Checks installed WOLAPI version and availability
- Manages registry keys for Generals installation

## Key Types
- OLEInitializer (Class): RAII wrapper for COM/OLE initialization
- IChat (Interface): WOLAPI COM interface (external)

## Key Functions
### getPathsFromRegistry
- Purpose: Retrieves Generals/WOLAPI install paths and serial from registry
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### setupGenerals
- Purpose: Writes Generals installation info to registry
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### checkInstalledWolapiVersion
- Purpose: Initializes WOLAPI and checks its version
- Calls: _Module.Init, CoCreateInstance, g_pChat->GetVersion, g_pChat->Release, _Module.Term, getPathsFromRegistry

## Globals
- _Module (CComModule): COM module instance
- g_wolapiRegistryVersion (unsigned long): Expected WOLAPI version
- g_wolapiRealVersion (unsigned long): Actual installed WOLAPI version
- g_wolapiInstalled (bool): WOLAPI availability flag
- g_wolapiRegFilename (char[MAX_PATH]): WOLAPI registry path
- g_wolapiRealFilename (char[MAX_PATH]): Actual WOLAPI DLL path
- g_generalsFilename (char[MAX_PATH]): Generals install path
- g_generalsSerial (char[1024]): Generals serial number
- g_OLEInitializer (OLEInitializer): Global COM/OLE initializer
- g_pChat (IChat*): WOLAPI COM interface pointer

## Dependencies
- Windows Registry API (winreg.h)
- ATL COM (atlbase.h, atlcom.h)
- WOLAPI headers (wolapi.h)
- wolSetup.h (project headers)
