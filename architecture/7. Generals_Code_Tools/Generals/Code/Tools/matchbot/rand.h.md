# Generals/Code/Tools/matchbot/rand.h

## Purpose
Header file defining a random number generator class for the matchbot tool.

## Responsibilities
- Provides random number generation utilities
- Supports both integer and floating-point random values
- Manages internal seed state for randomness

## Key Types
- RandClass (Class): Random number generator with configurable range

## Key Functions
### RandClass::RandClass
- Purpose: Constructor initializes the random seed.
- Calls: Not inferable.

### RandClass::Int
- Purpose: Returns a random integer.
- Calls: Not inferable.

### RandClass::Double
- Purpose: Returns a random floating-point value.
- Calls: Not inferable.

### RandClass::Int (overload)
- Purpose: Returns a random integer within a specified range.
- Calls: Not inferable.

### RandClass::Double (overload)
- Purpose: Returns a random floating-point value within a specified range.
- Calls: Not inferable.

### RandClass::randomValue
- Purpose: Generates the next random value.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `<cstdlib>` for standard library functions
