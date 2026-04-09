# Generals/Code/Libraries/Source/WWVegas/WWLib/RANDOM.H

## Purpose
Provides random number generation utilities for the game engine.

## Responsibilities
- Defines multiple random number generator classes with varying quality/speed tradeoffs
- Implements a template function for picking random numbers within a range
- Supports 15-bit to 32-bit random number generation

## Key Types
- **RandomClass (class)**: 15-bit random number generator using linear congruential algorithm
- **Random2Class (class)**: 32-bit fast random number generator using lookup table
- **Random3Class (class)**: 32-bit cryptographically strong random number generator
- **Random4Class (class)**: 32-bit Mersenne Twister implementation for high-quality randomness
- **Pick_Random_Number (template function)**: Utility for selecting random numbers within a range

## Key Functions
### Pick_Random_Number
- Purpose: Generates a random number within a specified range using a given random number generator
- Calls: generator() operator

## Globals
- None

## Dependencies
- Key includes: None (header-only)
- External symbols: None
