# Generals/Code/Tools/Launcher/DatGen/DatGen.cpp

## Purpose
Generates a passkey and encrypts data into Generals.dat for game activation.

## Responsibilities
- Reads game install path and serial from registry
- Retrieves hard drive serial number and Windows Product ID
- Generates a passkey and encrypts a fixed message using Blowfish
- Writes encrypted data to Generals.dat

## Key Types
- BlowfishEngine (Class): Blowfish encryption engine
- None (Other types)

## Key Functions
### doIt
- Purpose: Main function that generates passkey and encrypts data
- Calls: RegOpenKeyEx, RegQueryValueEx, GetVolumeInformation, BlowfishEngine::Submit_Key, BlowfishEngine::Encrypt, fopen, fwrite, fclose

### WinMain
- Purpose: Entry point that calls doIt
- Calls: doIt

## Globals
- CDAPFN_DECLARE_GLOBAL(doIt, CDAPFN_OVERHEAD_L5, CDAPFN_CONSTRAINT_NONE) (Macro): Declares doIt as a CDAPFN global

## Dependencies
- windows.h, assert.h, stdlib.h, stdio.h
- bfish.h (BlowfishEngine)
- SafeDisk/CdaPfn.h (CDAPFN macros)
- Debug/DebugPrint.h (DebugPrint)
