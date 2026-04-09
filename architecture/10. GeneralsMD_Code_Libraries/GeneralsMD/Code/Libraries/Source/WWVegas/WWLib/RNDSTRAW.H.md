# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RNDSTRAW.H

## Purpose
Declares the `RandomStraw` class, a straw terminator that generates random numbers to fulfill data requests.

## Responsibilities
- Generates random data on demand
- Manages seed bits and random number generators
- Provides seeding methods for different data types
- Ensures infinite random data supply

## Key Types
- `RandomStraw` (Class): Random data generator straw terminator
- `Random3Class` (Type): Underlying random number generator

## Key Functions
### `Get(void * source, int slen)`
- Purpose: Fills the provided buffer with random data
- Calls: Not inferable

### `Reset(void)`
- Purpose: Resets the random generator state
- Calls: Not inferable

### `Seed_Bit(int seed)`
- Purpose: Seeds the generator with a single bit
- Calls: Not inferable

### `Seed_Byte(char seed)`
- Purpose: Seeds the generator with a byte
- Calls: Not inferable

### `Seed_Short(short seed)`
- Purpose: Seeds the generator with a short
- Calls: Not inferable

### `Seed_Long(long seed)`
- Purpose: Seeds the generator with a long
- Calls: Not inferable

### `Seed_Bits_Needed(void)`
- Purpose: Returns the number of seed bits needed
- Calls: Not inferable

### `Scramble_Seed(void)`
- Purpose: Scrambles the seed data
- Calls: Not inferable

## Globals
- None

## Dependencies
- `random.h`
- `straw.h`
- `Random3Class` (external)
