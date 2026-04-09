# GeneralsMD/Code/GameEngine/Include/Common/BitFlags.h

## Purpose
Wrapper class for std::bitset to provide more intuitive initialization and bit manipulation operations.

## Responsibilities
- Provides type-safe bit flag operations
- Supports named bit flags via string lookup
- Serialization/deserialization via INI and Xfer
- Bitwise operations (set, clear, test, flip, etc.)

## Key Types
- **BitFlags (Class)**: Wrapper for std::bitset with improved constructors and named bit support
- **BogusInitType (Enum)**: Syntactic sugar to prevent implicit int-to-bitset conversion

## Key Functions
### BitFlags(BogusInitType, Int...)
- Purpose: Initialize with specific bits set
- Calls: m_bits.set()

### testForAny(const BitFlags&)
- Purpose: Check if any bits are set in both flags
- Calls: m_bits.&=

### testForAll(const BitFlags&)
- Purpose: Check if all bits in 'that' are set in this
- Calls: m_bits.flip(), m_bits.&=

### testSetAndClear(const BitFlags&, const BitFlags&)
- Purpose: Verify bits that must be set/clear
- Calls: m_bits.&=

### setBitByName(const char*)
- Purpose: Set a bit by its string name
- Calls: getSingleBitFromName(), set()

### parse(INI*, AsciiString*)
- Purpose: Parse bit flags from INI file
- Calls: Not inferable

## Globals
- **s_bitNameList (const char**)**: Array of bit names for this flag type

## Dependencies
- **INCLUDES**: Common/STLTypedefs.h
- **CLASSES**: INI, Xfer, AsciiString
- **STL**: std::bitset
