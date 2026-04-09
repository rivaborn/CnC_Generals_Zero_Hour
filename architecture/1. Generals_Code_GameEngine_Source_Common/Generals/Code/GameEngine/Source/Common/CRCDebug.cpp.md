# Generals/Code/GameEngine/Source/Common/CRCDebug.cpp

## Purpose
This file contains code for CRC (Cyclic Redundancy Check) debugging in the Command & Conquer Generals game engine. It logs and verifies CRC values to ensure data integrity during gameplay.

## Responsibilities
- Manages CRC verification for client-side logic.
- Logs debug information related to CRC checks.
- Dumps debug lines to a file for analysis.

## Key Types
- None

## Key Functions
### CRCVerification::CRCVerification
- Purpose: Initializes the start CRC value if debugging is enabled and conditions are met.
- Calls: TheGameLogic->getCRC, DEBUG_ASSERTCRASH

### CRCVerification::~CRCVerification
- Purpose: Verifies the end CRC value against the start CRC to ensure no changes occurred outside of expected updates.
- Calls: TheGameLogic->getCRC, TheInGameUI->message, CRCDEBUG_LOG

### outputCRCDebugLines
- Purpose: Outputs collected debug lines to a file named `crcDebug<MachineName>.txt`.
- Calls: fopen, fprintf, fclose

### addCRCDebugLine
- Purpose: Adds formatted debug information to the internal buffer if conditions are met.
- Calls: vsnprintf

### dumpVector3, dumpCoord3D, dumpMatrix3D, dumpReal
- Purpose: Dumps specific data types (Vector3, Coord3D, Matrix3D, Real) with their values and metadata to the debug log.

## Globals
- DebugStrings[MaxStrings][1024] (char): Buffer for storing debug lines.
- nextDebugString (Int): Index for the next debug line in the buffer.
- numDebugStrings (Int): Number of debug strings currently stored.
- dumped (Bool): Flag indicating if debug lines have been output.

## Dependencies
- Key includes: "Common/CRCDebug.h", "Common/Debug.h", "Common/PerfTimer.h", "GameClient/InGameUI.h", "GameNetwork/IPEnumeration.h"
- External symbols: TheGameLogic, g_verifyClientCRC, g_clientDeepCRC, TheDebugIgnoreSyncErrors, TheCRCFirstFrameToLog, TheCRCLastFrameToLog, TheInGameUI
