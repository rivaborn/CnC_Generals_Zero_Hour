# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/random.cpp

## Purpose
Implements multiple random number generator classes for game use.

## Responsibilities
- Provides 4 different RNG implementations (RandomClass, Random2Class, Random3Class, Random4Class)
- Supports both bounded and unbounded random number generation
- Includes performance-tested algorithms with statistical analysis
- Handles seed initialization and state management

## Key Types
- RandomClass (class): Basic 15-bit RNG using linear congruential method
- Random2Class (class): XOR-shift based RNG with table lookup
- Random3Class (class): 32-bit RNG with mixing tables for cryptographic strength
- Random4Class (class): Mersenne Twister implementation (N=624)
- Pick_Random_Number (function): Helper for bounded random number generation

## Key Functions
### RandomClass::operator()
- Purpose: Generates next random number in sequence
- Calls: None

### Random2Class::operator()
- Purpose: Generates random number via XOR table operations
- Calls: None

### Random3Class::operator()
- Purpose: Generates 32-bit random number using mixing tables
- Calls: None

### Random4Class::operator()
- Purpose: Implements Mersenne Twister algorithm
- Calls: None

### Pick_Random_Number
- Purpose: Generates random number within specified range
- Calls: Uses provided RNG object

## Globals
- Random3Class::Mix1[20] (int[]): First mixing table for Random3Class
- Random3Class::Mix2[20] (int[]): Second mixing table for Random3Class

## Dependencies
- "always.h", "random.h"
- ARRAY_SIZE macro
- Standard C++ types (int, unsigned, float)
