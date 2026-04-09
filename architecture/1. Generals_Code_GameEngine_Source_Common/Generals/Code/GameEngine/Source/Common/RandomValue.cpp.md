# Generals/Code/GameEngine/Source/Common/RandomValue.cpp

## Purpose
This file contains implementations for pseudo-random number generators used in the game engine, including functions to initialize seeds and generate random values for different components like GameLogic, GameClient, and GameAudio.

## Responsibilities
- Initialize random seeds.
- Generate integer and real-valued random numbers.
- Provide deterministic random sequences for debugging.

## Key Types
- None

## Key Functions
### randomValue
- Purpose: Generates a pseudo-random number using an internal seed array.
- Calls: `ADC`

### seedRandom
- Purpose: Seeds the random number generator with a given value.
- Calls: None

### GetGameLogicRandomSeed
- Purpose: Returns the base seed for GameLogic random numbers.
- Calls: None

### GetGameLogicRandomSeedCRC
- Purpose: Computes and returns a CRC of the GameLogic seed array.
- Calls: `computeCRC`, `get`

### InitRandom
- Purpose: Initializes random seeds based on time or a fixed value for deterministic behavior.
- Calls: `seedRandom`

### InitGameLogicRandom
- Purpose: Initializes the GameLogic random seed.
- Calls: `seedRandom`

### GetGameLogicRandomValue
- Purpose: Generates an integer random number within a specified range for GameLogic.
- Calls: `randomValue`

### GetGameClientRandomValue
- Purpose: Generates an integer random number within a specified range for GameClient.
- Calls: `randomValue`

### GetGameAudioRandomValue
- Purpose: Generates an integer random number within a specified range for GameAudio.
- Calls: `randomValue`

### GetGameLogicRandomValueReal
- Purpose: Generates a real-valued random number within a specified range for GameLogic.
- Calls: `randomValue`

### GetGameClientRandomValueReal
- Purpose: Generates a real-valued random number within a specified range for GameClient.
- Calls: `randomValue`

### GetGameAudioRandomValueReal
- Purpose: Generates a real-valued random number within a specified range for GameAudio.
- Calls: `randomValue`

## Globals
- theMultFactor (Real): Multiplier for converting integer random values to real numbers.
- theGameClientSeed (UnsignedInt[6]): Seed array for GameClient random numbers.
- theGameAudioSeed (UnsignedInt[6]): Seed array for GameAudio random numbers.
- theGameLogicBaseSeed (UnsignedInt): Base seed for GameLogic random numbers.
- theGameLogicSeed (UnsignedInt[6]): Seed array for GameLogic random numbers.

## Dependencies
- Key includes: "Lib/BaseType.h", "Common/RandomValue.h", "Common/CRC.h", "Common/Debug.h", "GameLogic/GameLogic.h"
- External symbols used: `powf`, `time`, `CRC::computeCRC`, `CRC::get`, `DEBUG_LOG`, `
