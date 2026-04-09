# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RANDOM.H

## Purpose
Provides random number generation utilities for the game engine.

## Responsibilities
- Defines multiple random number generator classes with varying quality/speed tradeoffs
- Implements a template function for picking random numbers within a range
- Supports different random number algorithms (linear congruential, table-based, Mersenne Twister)

## Key Types
- **RandomClass (class)**: Basic 15-bit random number generator using linear congruential algorithm
- **Random2Class (class)**: Faster 32-bit random number generator using table lookup
- **Random3Class (class)**: Higher-quality 32-bit random number generator with better statistical properties
- **Random4Class (class)**: Mersenne Twister-based 32-bit random number generator with very long period
- **Pick_Random_Number (template function)**: Utility for selecting random numbers within a specified range

## Key Functions
### Pick_Random_Number
- Purpose: Returns a random number between minval and maxval (inclusive) using the provided generator
- Calls: generator() operator

## Globals
- None

## Dependencies
- Key includes: None (header-only)
- External symbols: None
