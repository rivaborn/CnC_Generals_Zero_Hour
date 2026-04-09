# GeneralsMD/Code/GameEngine/Source/Common/RandomValue.cpp

## Purpose
Implements pseudo-random number generators for game logic, client, and audio systems.

## Responsibilities
- Provides deterministic and non-deterministic random number generation
- Separates random streams for game logic, client, and audio
- Supports integer and real-valued random distributions
- Manages random variable classes for game logic and client

## Key Types
- `GameClientRandomVariable` (Class): Encapsulates client-side random value generation with distribution types
- `GameLogicRandomVariable` (Class): Encapsulates logic-side random value generation with distribution types
- `DistributionType` (Enum): Defines types of random distributions (CONSTANT, UNIFORM, GAUSSIAN, etc.)

## Key Functions
### `randomValue`
- Purpose: Core pseudo-random number generator using a 6-word seed array
- Calls: None (uses macros ADC and direct array operations)

### `seedRandom`
- Purpose: Initializes the random seed array from a base seed value
- Calls: None

### `GetGameLogicRandomValue`
- Purpose: Returns a random integer in [lo, hi] for game logic
- Calls: `randomValue`

### `GetGameClientRandomValue`
- Purpose: Returns a random integer in [lo, hi] for game client
- Calls: `randomValue`

### `GetGameLogicRandomValueReal`
- Purpose: Returns a random real number in [lo, hi] for game logic
- Calls: `randomValue`

### `InitRandom`
- Purpose: Initializes all random seed arrays (deterministic or time-based)
- Calls: `seedRandom`

### `InitGameLogicRandom`
- Purpose: Initializes only the game logic random seed
- Calls: `seedRandom`

## Globals
- `theMultFactor` (Real): Scaling factor for real-valued random numbers
- `theGameClientSeed` (UnsignedInt[6]): Seed array for client-side randomness
- `theGameAudioSeed` (UnsignedInt[6]): Seed array for audio-side randomness
- `theGameLogicBaseSeed` (UnsignedInt): Base seed for game logic randomness
- `theGameLogicSeed` (UnsignedInt[6]): Seed array for game logic randomness

## Dependencies
- `PreRTS.h`, `BaseType.h`, `RandomValue.h`, `CRC.h`, `Debug.h`, `GameLogic.h`
- `TheGameLogic` (external symbol from GameLogic.h)
