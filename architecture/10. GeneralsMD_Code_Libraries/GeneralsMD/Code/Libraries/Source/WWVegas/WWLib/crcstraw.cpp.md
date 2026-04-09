# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crcstraw.cpp

## Purpose
Implements a CRC (Cyclic Redundancy Check) calculation straw segment for data processing.

## Responsibilities
- Fetches data and calculates CRC on it
- Returns the CRC result of processed data
- Inherits from Straw base class

## Key Types
- CRCStraw (Class): CRC calculation straw segment

## Key Functions
### CRCStraw::Get
- Purpose: Fetch data and calculate CRC on it
- Calls: Straw::Get, CRC

### CRCStraw::Result
- Purpose: Return the CRC value of all processed data
- Calls: CRC

## Globals
- None

## Dependencies
- "always.h"
- "crcstraw.h"
- Straw base class
- CRC function (external)
