# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rng.h

## Purpose
Defines an abstract interface for a random number generator in the SAGE engine.

## Responsibilities
- Declares the `RandomNumberGenerator` abstract base class
- Defines the interface for retrieving random number blocks
- Provides virtual destructor for proper cleanup

## Key Types
- RandomNumberGenerator (Class): Abstract interface for random number generation

## Key Functions
### ~RandomNumberGenerator
- Purpose: Virtual destructor for the RandomNumberGenerator class
- Calls: None

### Get_Block
- Purpose: Pure virtual function to retrieve a block of random numbers
- Calls: None

## Globals
- None

## Dependencies
- None (header-only, no external includes or symbols)
