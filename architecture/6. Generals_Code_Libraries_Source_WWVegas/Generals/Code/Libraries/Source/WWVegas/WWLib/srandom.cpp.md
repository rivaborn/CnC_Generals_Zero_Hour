# Generals/Code/Libraries/Source/WWVegas/WWLib/srandom.cpp

## Purpose
Implements a secure random number generator using SHA hashing and system-specific entropy sources.

## Responsibilities
- Generates cryptographically secure random numbers
- Seeds the random number generator from system entropy
- Maintains a cache of random values for performance
- Provides XOR-based mixing with a fallback RNG

## Key Types
- SecureRandomClass (Class): Main random number generator
- Random3Class (Class): Fallback random number generator

## Key Functions
### SecureRandomClass::Add_Seeds
- Purpose: Adds external entropy to the seed pool
- Calls: None

### SecureRandomClass::Randval
- Purpose: Returns a 32-bit random value
- Calls: SHAEngine::Hash, SHAEngine::Result, RandomHelper()

### SecureRandomClass::Generate_Seed
- Purpose: Initializes the seed pool from system entropy
- Calls: GetDiskFreeSpace, GetComputerName, GetUserName, time, getpid, GetTickCount

## Globals
- SecureRandomClass::Seeds (unsigned char[]): Seed material for SHA
- SecureRandomClass::Initialized (bool): Initialization flag
- SecureRandomClass::RandomCache (unsigned int[]): Cached random values
- SecureRandomClass::RandomCacheEntries (int): Cache size
- SecureRandomClass::Counter (unsigned int): Counter for seed rotation
- SecureRandomClass::RandomHelper (Random3Class): Fallback RNG

## Dependencies
- srandom.h, stdlib.h, stdio.h, time.h, assert.h, sha.h
- UNIX: osdep.h
- Windows: win.h, process.h
- External: SHAEngine, Random3Class
