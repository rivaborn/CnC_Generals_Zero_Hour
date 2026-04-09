# Generals/Code/Tools/mangler/endian.h

## Purpose
Provides endianness conversion utilities for network data handling in the game.

## Responsibilities
- Defines a global flag for big-endian systems.
- Implements a templated `Endian` function to swap byte order if needed.
- Supports network order (big-endian) and platform-specific endianness.

## Key Types
- None

## Key Functions
### `Endian<T>(val)`
- Purpose: Converts a value between host and network byte order if the system is big-endian.
- Calls: None (directly manipulates bytes via pointer arithmetic).

## Globals
- `BigEndian` (bool): Indicates whether the system uses big-endian byte order.

## Dependencies
- None (header-only, uses basic C++ types).
