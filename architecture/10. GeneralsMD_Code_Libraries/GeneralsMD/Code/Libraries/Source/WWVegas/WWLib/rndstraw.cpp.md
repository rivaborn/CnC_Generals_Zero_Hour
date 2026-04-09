# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rndstraw.cpp

## Purpose
Implements a cryptographically secure random number generator using the SHA-1 algorithm.

## Responsibilities
- Seeds the random number generator with external entropy
- Generates random bytes via SHA-1 hashing
- Manages internal state and scrambling of seed data
- Provides interface for feeding random bits/bytes/words

## Key Types
- `RandomStraw` (Class): Cryptographically secure random number generator
- `SHAEngine` (External): Used for scrambling seed data

## Key Functions
### `RandomStraw::Seed_Bit`
- Purpose: Adds a single random bit to the seed
- Calls: None

### `RandomStraw::Seed_Byte`
- Purpose: Feeds 8 bits into the seed
- Calls: `Seed_Bit`

### `RandomStraw::Seed_Short`
- Purpose: Feeds 16 bits into the seed
- Calls: `Seed_Bit`

### `RandomStraw::Seed_Long`
- Purpose: Feeds 32 bits into the seed
- Calls: `Seed_Bit`

### `RandomStraw::Scramble_Seed`
- Purpose: Applies SHA-1 to scramble accumulated seed bits
- Calls: `SHAEngine::Hash`, `SHAEngine::Result`

### `RandomStraw::Get`
- Purpose: Generates random bytes from the current state
- Calls: `Straw::Get` (fallback)

## Globals
- `Random` (Array): Internal seed/state buffer
- `SeedBits` (int): Count of accumulated seed bits
- `Current` (int): Current position in random buffer

## Dependencies
- `rndstraw.h`: Class declaration
- `sha.h`: SHA-1 hashing interface
- `always.h`: Likely common headers
- `<limits.h>`: For `CHAR_BIT`
- `<string.h>`: For `memset`, `memmove`
