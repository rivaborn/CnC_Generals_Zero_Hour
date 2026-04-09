# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AutoHealBehavior.h

## Purpose
Defines the AutoHealBehavior module for automatic healing of objects in the game.

## Responsibilities
- Implements automatic healing behavior for objects
- Handles healing upgrades and particle effects
- Manages healing delays and radius-based healing
- Processes damage events and healing states
- Supports configuration via module data

## Key Types
- **AutoHealBehaviorModuleData (Class)**: Configuration data for healing behavior
- **AutoHealBehavior (Class)**: Main healing behavior module
- **AutoHealBehaviorMagicEnum (Enum)**: Not inferable
- **ParticleSystem (Class)**: External particle system reference
- **ParticleSystemTemplate (Class)**: External particle system template reference

## Key Functions
### AutoHealBehaviorModuleData::buildFieldParse
- Purpose: Defines INI field parsing for module data
- Calls: None

### AutoHealBehavior::onDamage
- Purpose: Handles damage events and healing initiation
- Calls: Not inferable

### AutoHealBehavior::update
- Purpose: Updates healing state and performs healing
- Calls: Not inferable

### AutoHealBehavior::pulseHealObject
- Purpose: Applies healing to a specific object
- Calls: Not inferable

## Globals
- None

## Dependencies
- "GameClient/ParticleSys.h"
- "GameLogic/Module/BehaviorModule.h"
- "GameLogic/Module/UpgradeModule.h"
- "GameLogic/Module/UpdateModule.h"
- "GameLogic/Module/DamageModule.h"
- "Common/BitFlagsIO.h"
- ParticleSystem, ParticleSystemTemplate classes
