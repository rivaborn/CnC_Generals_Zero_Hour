# GeneralsMD/Code/GameEngine/Include/GameClient/ClientRandomValue.h

## Purpose
Declares client-side random number generation utilities and the `GameClientRandomVariable` class for distributed random values.

## Responsibilities
- Provides macros for client-side random value generation.
- Defines `GameClientRandomVariable` for configurable random distributions.
- Declares distribution types (constant, uniform, Gaussian, etc.).
- Exposes range and value retrieval methods.

## Key Types
- **GameClientRandomVariable (Class)**: Manages random value distributions with configurable ranges and types.
- **DistributionType (Enum)**: Defines distribution types (CONSTANT, UNIFORM, GAUSSIAN, TRIANGULAR, LOW_BIAS, HIGH_BIAS).

## Key Functions
### `GetGameClientRandomValue`
- Purpose: Generates a random integer in a specified range.
- Calls: None (external implementation).

### `GetGameClientRandomValueReal`
- Purpose: Generates a random real number in a specified range.
- Calls: None (external implementation).

## Globals
- **DistributionTypeNames (const char\*)**: Array of distribution type names (external definition).

## Dependencies
- `Lib/BaseType.h` (for `Int` and `Real` types).
- Forward declarations: `CColorAlphaDialog`, `DebugWindowDialog`.
