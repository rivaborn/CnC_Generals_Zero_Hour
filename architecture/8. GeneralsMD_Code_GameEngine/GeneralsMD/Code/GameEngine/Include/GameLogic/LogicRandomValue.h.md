# GeneralsMD/Code/GameEngine/Include/GameLogic/LogicRandomValue.h

## Purpose
Header defining random number generation utilities and the `GameLogicRandomVariable` class for distributed random values.

## Responsibilities
- Declares random value generation functions and macros
- Defines `GameLogicRandomVariable` for configurable random distributions
- Provides distribution type enum and helper methods

## Key Types
- **GameLogicRandomVariable (Class)**: Manages random value distributions (uniform, Gaussian, etc.)
- **DistributionType (Enum)**: Defines supported distribution types (CONSTANT, UNIFORM, GAUSSIAN, TRIANGULAR, LOW_BIAS, HIGH_BIAS)

## Key Functions
### GetGameLogicRandomValue
- Purpose: Generates a random integer in [lo, hi)
- Calls: Not inferable

### GetGameLogicRandomValueReal
- Purpose: Generates a random real number in [lo, hi)
- Calls: Not inferable

## Globals
- **DistributionTypeNames (const char\*)**: Array of distribution type names (static)

## Dependencies
- `Lib/BaseType.h` (for Int/Real types)
- Forward declarations: `CColorAlphaDialog`, `DebugWindowDialog`
