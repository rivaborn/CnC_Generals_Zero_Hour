# GeneralsMD/Code/GameEngine/Source/Common/CRCDebug.cpp

## Purpose
Handles CRC (Cyclic Redundancy Check) debugging and logging for game state verification.

## Responsibilities
- Manages CRC verification for game logic updates
- Logs debug strings for CRC verification
- Dumps debug information to files
- Provides macros for dumping various data types (Vector3, Coord3D, Matrix3D, Real)

## Key Types
- CRCVerification (Class): Tracks CRC values for game logic verification
- None (other types are basic or external)

## Key Functions
### CRCVerification::CRCVerification()
- Purpose: Initializes CRC verification by capturing the current game state CRC
- Calls: TheGameLogic->getCRC()

### CRCVerification::~CRCVerification()
- Purpose: Verifies game state CRC hasn't changed unexpectedly during update
- Calls: TheGameLogic->getCRC(), TheInGameUI->message(), CRCDEBUG_LOG()

### addCRCDebugLine()
- Purpose: Adds a formatted debug string to the CRC debug log
- Calls: sprintf(), _vsnprintf()

### dumpVector3/dumpCoord3D/dumpMatrix3D/dumpReal()
- Purpose: Dumps specific data types to the CRC debug log with metadata
- Calls: addCRCDebugLine()

## Globals
- DebugStrings (char[MaxStrings][1024]): Circular buffer for debug strings
- nextDebugString/numDebugStrings (Int): Track debug string buffer state
- dumped (Bool): Flag to prevent duplicate output
- lastCRCDebugFrame/lastCRCDebugIndex (Int): Track frame/line for debug output

## Dependencies
- Common/CRCDebug.h, Common/Debug.h, Common/PerfTimer.h
- GameClient/InGameUI.h, GameNetwork/IPEnumeration.h
- TheGameLogic, TheInGameUI, g_verifyClientCRC, g_clientDeepCRC, TheDebugIgnoreSyncErrors, TheCRCFirstFrameToLog, TheCRCLastFrameToLog
