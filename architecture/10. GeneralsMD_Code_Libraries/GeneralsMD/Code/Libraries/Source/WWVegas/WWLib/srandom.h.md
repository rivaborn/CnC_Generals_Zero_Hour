# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/srandom.h

## Purpose
Declares the `SecureRandomClass` for cryptographically suitable random number generation.

## Responsibilities
- Provides secure random number generation via `Randval()`.
- Manages seed generation and pooling via `Add_Seeds()` and `Generate_Seed()`.
- Maintains internal state for randomness caching and counter.

## Key Types
- **SecureRandomClass (Class)**: Secure random number generator.
- **(anonymous enum) (Enum)**: Defines constants for seed and digest lengths.
- **SeedLength (Enum)**: Length of random seed in bytes (16).
- **SHADigestBytes (Enum)**: Length of SHA hash in bytes (20).

## Key Functions
### SecureRandomClass::Randval
- Purpose: Returns a 32-bit secure random value.
- Calls: Not inferable.

### SecureRandomClass::Add_Seeds
- Purpose: Adds entropy to the seed pool.
- Calls: Not inferable.

### SecureRandomClass::Generate_Seed
- Purpose: Generates the initial seed.
- Calls: Not inferable.

## Globals
- **Initialized (bool)**: Tracks if the seed is initialized.
- **Seeds (unsigned char[16])**: Stores the random seed.
- **RandomCache (unsigned int[5])**: Caches random values.
- **RandomCacheEntries (int)**: Count of cached entries.
- **Counter (unsigned int)**: Incremental counter for randomness.
- **RandomHelper (Random3Class)**: Helper RNG instance.

## Dependencies
- `random.h` (for `Random3Class`).
