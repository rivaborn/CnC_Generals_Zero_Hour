# GeneralsMD/Code/GameEngine/Include/Common/BitFlagsIO.h

## Purpose
Provides I/O functionality for the BitFlags template class, including INI parsing and Xfer serialization.

## Responsibilities
- INI file parsing for BitFlags
- Xfer serialization/deserialization for BitFlags
- Bit flag name resolution and validation

## Key Types
- BitFlags<NUMBITS> (template class): bit flag container with I/O operations

## Key Functions
### BitFlags<NUMBITS>::parse
- Purpose: Parses bit flags from INI tokens with support for +/-
- Calls: INI::scanIndexList, set, clear, DEBUG_CRASH

### BitFlags<NUMBITS>::parseFromINI
- Purpose: Static INI parser entry point for BitFlags
- Calls: parse

### BitFlags<NUMBITS>::parseSingleBitFromINI
- Purpose: Parses single bit index from INI
- Calls: INI::scanIndexList

### BitFlags<NUMBITS>::xfer
- Purpose: Handles Xfer serialization/deserialization/CRC
- Calls: XferVersion, xferVersion, xferInt, xferAsciiString, setBitByName, DEBUG_CRASH

## Globals
None

## Dependencies
- Common/BitFlags.h
- Common/INI.h
- Common/Xfer.h
