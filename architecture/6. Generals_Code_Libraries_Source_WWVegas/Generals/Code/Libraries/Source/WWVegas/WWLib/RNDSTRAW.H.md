# Generals/Code/Libraries/Source/WWVegas/WWLib/RNDSTRAW.H

## Purpose
Declares the `RandomStraw` class, a straw terminator that generates random numbers for data requests.

## Responsibilities
- Generates random numbers to fill data requests
- Manages random number seed bits
- Provides methods to seed the random number generator
- Implements scrambling of the seed for security

## Key Types
- **RandomStraw (Class)**: A straw terminator that generates random numbers
- **Random3Class (Type)**: Underlying random number generator (external)

## Key Functions
### RandomStraw::Get
- Purpose: Retrieves random data into the provided buffer
- Calls: Not inferable (implementation in .cpp)

### RandomStraw::Seed_Bit
- Purpose: Seeds the generator with a single bit
- Calls: Not inferable

### RandomStraw::Seed_Byte
- Purpose: Seeds the generator with a byte
- Calls: Not inferable

### RandomStraw::Seed_Short
- Purpose: Seeds the generator with a short
- Calls: Not inferable

### RandomStraw::Seed_Long
- Purpose: Seeds the generator with a long
- Calls: Not inferable

### RandomStraw::Scramble_Seed
- Purpose: Scrambles the seed for security
- Calls: Not inferable

## Globals
- None

## Dependencies
- `random.h` (for `Random3Class`)
- `straw.h` (base `Straw` class)
