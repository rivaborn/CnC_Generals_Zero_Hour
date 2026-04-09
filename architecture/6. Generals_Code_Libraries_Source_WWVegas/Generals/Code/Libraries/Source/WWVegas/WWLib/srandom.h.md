# Generals/Code/Libraries/Source/WWVegas/WWLib/srandom.h

## Purpose
Declares the `SecureRandomClass` for cryptographically suitable random number generation.

## Responsibilities
- Provides secure random number generation via `Randval()`
- Manages seed initialization and augmentation via `Add_Seeds()`
- Handles platform-specific seed generation (UNIX vs. Windows)
- Maintains an internal random cache for performance

## Key Types
- **SecureRandomClass (Class)**: Secure random number generator.
- **(anonymous enum) (Enum)**: Defines internal constants (`SeedLength`, `SHADigestBytes`).
- **SeedLength (Enum)**: Length of random seed in bytes (16).
- **SHADigestBytes (Enum)**: Length of SHA hash in bytes (20).

## Key Functions
### SecureRandomClass::Randval
- Purpose: Returns a 32-bit secure random value.
- Calls: Not inferable (implementation in .cpp).

### SecureRandomClass::Add_Seeds
- Purpose: Adds entropy to the seed pool from external data.
- Calls: Not inferable.

### SecureRandomClass::Generate_Seed
- Purpose: Generates the initial seed (called during construction).
- Calls: Not inferable.

## Globals
- **Initialized (bool)**: Tracks if the seed has been initialized.
- **Seeds (unsigned char[16])**: Stores the random seed.
- **RandomCache (unsigned int[5])**: Caches random values for performance.
- **RandomCacheEntries (int)**: Tracks valid entries in `RandomCache`.
- **Counter (unsigned int)**: Used in seed generation.
- **RandomHelper (Random3Class)**: Helper RNG instance.

## Dependencies
- `random.h`: For `Random3Class` (helper RNG).
- SHA-1 hashing (implied by `SHADigest
