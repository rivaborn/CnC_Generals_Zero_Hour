# GeneralsMD/Code/GameEngine/Include/Common/AcademyStats.h

## Purpose
Manages player statistics for providing in-game advice and guidance.

## Responsibilities
- Tracks player actions (buildings, upgrades, special powers)
- Evaluates player performance across three tiers (basic, intermediate, advanced)
- Generates advice tips based on collected statistics
- Supports snapshot serialization for game state saving

## Key Types
- **AcademyAdviceInfo (struct)**: Holds advice tips and count
- **AcademyClassificationType (enum)**: Classifies advice types (none, radar upgrade, superpower)
- **AcademyStats (class)**: Main statistics tracker with advice generation

## Key Functions
### `calculateAcademyAdvice`
- Purpose: Generates advice tips based on collected statistics
- Calls: `evaluateTier1Advice`, `evaluateTier2Advice`, `evaluateTier3Advice`

### `recordProduction`
- Purpose: Records unit/building production events
- Calls: None

### `recordSpecialPowerUsed`
- Purpose: Tracks usage of special powers
- Calls: None

### `evaluateTier1Advice`
- Purpose: Evaluates basic player performance metrics
- Calls: None

## Globals
- **TheAcademyClassificationTypeNames (const char**)**: String names for advice classification types

## Dependencies
- `Lib/BaseType.h`, `Common/Debug.h`, `Common/Snapshot.h`, `Common/UnicodeString.h`
- External classes: `Object`, `Player`, `SpecialPowerTemplate`, `UpgradeTemplate`, `CommandSet`, `ThingTemplate`
