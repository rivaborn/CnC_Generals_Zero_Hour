# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GrantStealthBehavior.h

## Purpose
Defines a behavior module that grants permanent stealth to objects whose stealth is permanently grantable.

## Responsibilities
- Manages stealth granting logic for objects
- Handles particle system effects for visual feedback
- Processes configuration data for stealth behavior
- Updates stealth state over time

## Key Types
- **GrantStealthBehaviorModuleData (Class)**: Configuration data for stealth behavior
- **GrantStealthBehavior (Class)**: Behavior module that grants stealth to objects
- **GrantStealthBehaviorMagicEnum (Enum)**: Not inferable
- **GrantStealthBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### GrantStealthBehaviorModuleData::buildFieldParse
- Purpose: Parses configuration data from INI files
- Calls: UpdateModuleData::buildFieldParse

### GrantStealthBehavior::update
- Purpose: Updates stealth behavior state
- Calls: Not inferable

### GrantStealthBehavior::grantStealthToObject
- Purpose: Applies stealth to a specific object
- Calls: Not inferable

## Globals
- None

## Dependencies
- GameClient/ParticleSys.h
- GameLogic/Module/BehaviorModule.h
- GameLogic/Module/UpgradeModule.h
- GameLogic/Module/UpdateModule.h
- GameLogic/Module/DamageModule.h
- Common/BitFlagsIO.h
