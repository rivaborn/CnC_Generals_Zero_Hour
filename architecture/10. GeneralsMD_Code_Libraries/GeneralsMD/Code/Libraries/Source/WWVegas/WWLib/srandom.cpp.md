# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/srandom.cpp

## Purpose
Implements a secure random number generator using SHA hashing and system-specific entropy sources.

## Responsibilities
- Generates cryptographically stronger random numbers via SHA hashing
- Seeds the generator using system entropy (OS-specific)
- Provides a cached random value pool for performance
- Mixes output with a simpler RNG for better distribution

## Key Types
- SecureRandomClass (Class): Main secure random number generator
- Random3Class (Class): Fallback simple RNG helper

## Key Functions
### SecureRandomClass::Add_Seeds
- Purpose: Mix additional entropy into the seed pool
- Calls: None

### SecureRandomClass::Randval
- Purpose: Returns a 32-bit secure random value
- Calls: SHAEngine::Hash, SHAEngine::Result, RandomHelper()

### SecureRandomClass::Generate_Seed
- Purpose: Initializes the seed pool using system entropy
- Calls: GetDiskFreeSpace, GetComputerName, GetUserName, time, getpid, GetTickCount

## Globals
- SecureRandomClass::Seeds (unsigned char[]): Primary seed pool
- SecureRandomClass::RandomCache (unsigned int[]): Cached random values
- SecureRandomClass::Counter (unsigned int): Monotonic counter for seed mixing
- SecureRandomClass::RandomHelper (Random3Class): Fallback RNG instance

## Dependencies
- sha.h (SHAEngine)
- stdlib.h, time.h, assert.h
- OS-specific headers (win.h/osdep.h)
