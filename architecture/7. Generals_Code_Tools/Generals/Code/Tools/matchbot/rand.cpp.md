# Generals/Code/Tools/matchbot/rand.cpp

## Purpose
Implements a pseudo-random number generator (PRNG) using a custom algorithm.

## Responsibilities
- Initialize PRNG state with a seed
- Generate random integers and doubles
- Provide bounded random number generation

## Key Types
- `RandClass` (Class): PRNG implementation
- `theMultFactor` (const double): Scaling factor for double generation

## Key Functions
### `RandClass::RandClass(int start)`
- Purpose: Initialize PRNG with a seed value
- Calls: None

### `RandClass::randomValue()`
- Purpose: Generate next random unsigned integer
- Calls: None

### `RandClass::Int()`
- Purpose: Generate random integer
- Calls: `randomValue()`

### `RandClass::Int(int low, int high)`
- Purpose: Generate random integer in range [low, high]
- Calls: `randomValue()`

### `RandClass::Double()`
- Purpose: Generate random double in [0.0, 1.0]
- Calls: `Double(0.0, 1.0)`

### `RandClass::Double(double low, double high)`
- Purpose: Generate random double in range [low, high]
- Calls: `randomValue()`

## Globals
- `theMultFactor` (const double): Scaling factor for double generation

## Dependencies
- `<cmath>` for `pow()` function
- `rand.h` for class declaration
