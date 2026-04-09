# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CreateCrateDie.h

## Purpose
Defines a game module that spawns a crate when an object dies, with configurable conditions.

## Responsibilities
- Spawns crates on object death
- Evaluates conditions (chance, veterancy, killer type/science)
- Parses crate data from INI files
- Manages module data and lifecycle

## Key Types
- **CrateTemplate (Class)**: Not inferable.
- **CreateCrateDieModuleData (Class)**: Holds crate name list and parsing logic.
- **CreateCrateDie (Class)**: Core module implementing crate spawning on death.
- **CreateCrateDieMagicEnum (Enum)**: Not inferable.
- **CreateCrateDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### CreateCrateDieModuleData::parseCrateData
- Purpose: Parses crate data from INI files.
- Calls: Not inferable.

### CreateCrateDie::onDie
- Purpose: Handles object death and triggers crate creation.
- Calls: testCreationChance, testVeterancyLevel, testKillerType, testKillerScience, createCrate.

### CreateCrateDie::testCreationChance
- Purpose: Checks if crate creation should proceed based on chance.
- Calls: Not inferable.

### CreateCrateDie::testVeterancyLevel
- Purpose: Validates veterancy level for crate creation.
- Calls: Not inferable.

### CreateCrateDie::testKillerType
- Purpose: Checks killer type against crate requirements.
- Calls: Not inferable.

### CreateCrateDie::testKillerScience
- Purpose: Verifies killer's science type for crate creation.
- Calls: Not inferable.

### CreateCrateDie::createCrate
