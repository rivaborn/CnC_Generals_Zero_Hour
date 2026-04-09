# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Weapon.cpp

## Purpose
Handles weapon behavior, templates, and networking for the game's combat system.

## Responsibilities
- Manages weapon templates and their properties
- Handles weapon firing logic and effects
- Implements networking serialization for weapons
- Provides utility functions for weapon calculations
- Manages weapon bonuses and conditions

## Key Types
- **WeaponTemplate (Class)**: Defines weapon properties and behavior
- **Weapon (Class)**: Runtime weapon instance with state
- **WeaponBonus (Class)**: Represents weapon stat bonuses
- **WeaponBonusSet (Class)**: Collection of weapon bonuses
- **AssistanceRequestData (Class)**: Data for requesting assistance
- **DistanceCalculationType (Enum)**: Type of distance calculation

## Key Functions
### parsePerVetLevelAsciiString
- Purpose: Parses veteran level-specific ASCII strings from INI
- Calls: INI::scanIndexList, INI::getNextAsciiString

### parseAllVetLevelsAsciiString
- Purpose: Parses ASCII strings applied to all veteran levels
- Calls: INI::getNextAsciiString

### parsePerVetLevelFXList
- Purpose: Parses veteran level-specific FX lists
- Calls: INI::parseFXList

### parseAllVetLevelsFXList
- Purpose: Parses FX lists applied to all veteran levels
- Calls: INI::parseFXList

### parsePerVetLevelPSys
- Purpose: Parses veteran level-specific particle systems
- Calls: INI::parseParticleSystemTemplate

### parseAllVetLevelsPSys
- Purpose: Parses particle systems applied to all veteran levels
- Calls: INI::parseParticleSystemTemplate

### is2DDistSquaredLessThan
- Purpose: Checks if 2D distance squared is less than a threshold
- Calls: None

### clipToTerrainExtent
- Purpose: Clips coordinates to terrain boundaries
- Calls: TheTerrainLogic->getTerrainExtent

### makeAssistanceRequest
- Purpose: Creates an assistance request for a weapon
- Calls: TheGameLogic->makeAssistanceRequest

### Weapon::crc
- Purpose: Serializes weapon state for networking
- Calls: Xfer methods

### Weapon::xfer
- Purpose: Network serialization for weapons
- Calls: Xfer methods

### WeaponBonus::appendBonuses
- Purpose: Applies weapon bonuses to another bonus
- Calls: None

### WeaponBonusSet::parseWeaponBonusSet
- Purpose: Parses weapon bonus sets from INI
- Calls: INI::scanIndexList, INI::scanPercentToReal

## Globals
- **ATTACK_RANGE_CALC_TYPE (const DistanceCalculationType)**: Attack range calculation type
- **DAMAGE_RANGE_CALC_TYPE (const DistanceCalculationType)**: Damage range calculation type
- **TheWeaponStore (WeaponStore*)**: Global weapon store instance

## Dependencies
- Common: CRC, GameAudio, GameState, INI, PerfTimer, Player, ThingFactory, ThingTemplate, Xfer
- GameClient: Drawable, FXList, InGameUI, ParticleSys
- GameLogic: Damage, ExperienceTracker, GameLogic, AIPathfind, Module classes, Object, ObjectCreationList, PartitionManager, Weapon
- GameLogic/Module: AIUpdate, AssistedTargetingUpdate, ProjectileStreamUpdate, PhysicsUpdate, TerrainLogic
