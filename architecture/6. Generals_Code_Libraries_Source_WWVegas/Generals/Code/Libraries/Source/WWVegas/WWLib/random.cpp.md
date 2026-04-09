# Generals/Code/Libraries/Source/WWVegas/WWLib/random.cpp

## Purpose
Implements multiple random number generator classes for the game engine.

## Responsibilities
- Provides four different random number generator implementations (RandomClass, Random2Class, Random3Class, Random4Class)
- Supports both bounded and unbounded random number generation
- Includes performance-tested algorithms with statistical analysis
- Handles seed initialization and random number distribution

## Key Types
- RandomClass (Class): Basic linear congruential generator
- Random2Class (Class): XOR-shift based generator
- Random3Class (Class): Cryptographically stronger generator with 64-bit seeding
- Random4Class (Class): Mersenne Twister implementation
- Pick_Random_Number (Function): Helper for range-based random number generation

## Key Functions
### RandomClass::operator()
- Purpose: Generates next random number in sequence
- Calls: None

### Random2Class::operator()
- Purpose: XOR-shift based random number generation
- Calls: None

### Random3Class::operator()
- Purpose: Cryptographically strong random number generation
- Calls: None

### Random4Class::operator()
- Purpose: Mersenne Twister random number generation
- Calls: None

### Pick_Random_Number
- Purpose: Generates random number within specified range
- Calls: Uses random number generator class operators

## Globals
- Random3Class::Mix1[20] (int[]): Predefined mixing values for Random3Class
- Random3Class::Mix2[20] (int[]): Additional mixing values for Random3Class

## Dependencies
- "always.h": Header for common definitions
- "random.h": Header containing class declarations
- ARRAY_SIZE: Macro for array size calculation
- Not inferable external symbols used
