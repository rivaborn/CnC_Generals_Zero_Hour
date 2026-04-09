# Generals/Code/Tools/Autorun/GetCD.h

## Purpose
Header file defining CD drive detection and volume verification functionality for the game's autorun system.

## Responsibilities
- Declares `GetCDClass` for CD drive enumeration
- Provides volume label verification functions
- Defines legacy RedBook audio functionality (Win95 only)
- Manages CD drive indexing and iteration

## Key Types
- `GetCDClass` (Class): CD drive enumeration and management
- `RedBookClass` (Class, Win95 only): Legacy CD audio playback
- `TinfoType`, `StatType`, `VolmType`, `PlayType`, `StopType` (Structs): Legacy audio control blocks
- `SEGSEL` (Struct): Segment selector for real mode calls

## Key Functions
### `CD_Volume_Verification`
- Purpose: Verify CD volume label matches expected label
- Calls: Not inferable

### `GetCDClass::Get_First_CD_Drive`
- Purpose: Initialize and return first CD drive
- Calls: `Get_Next_CD_Drive`

### `GetCDClass::Get_Next_CD_Drive`
- Purpose: Return next CD drive in sequence
- Calls: None

## Globals
- `_CD_Volume_Label` (char*): Array of expected volume labels
- `_Num_Volumes` (int): Number of volume labels to check
- `CDList` (GetCDClass): Global CD drive manager instance

## Dependencies
- Key includes: None (header-only)
- External symbols: DPMI real mode functions (Win95 only)
- Types: `UINT`, `USHORT`, `UBYTE`, `UWORD`, `ULONG` (legacy types)
