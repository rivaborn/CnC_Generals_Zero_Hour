# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ActiveBody.h

## Purpose
Defines the ActiveBody module, which manages health, damage, and armor for game objects.

## Responsibilities
- Track health, damage states, and armor
- Handle damage, healing, and particle effects
- Manage subdual damage and indestructibility
- Validate armor and damage FX configurations

## Key Types
- **ActiveBodyModuleData (Class)**: Stores health and subdual damage parameters
- **ActiveBody (Class)**: Core class managing health, damage, and armor
- **ActiveBodyMagicEnum (Enum)**: Not inferable (empty)
- **ActiveBody_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### attemptDamage
- Purpose: Apply damage to the object
- Calls: validateArmorAndDamageFX, doDamageFX, internalChangeHealth

### attemptHealing
- Purpose: Heal the object
- Calls: internalChangeHealth

### evaluateVisualCondition
- Purpose: Update visual state based on damage
- Calls: setCorrectDamageState

### updateBodyParticleSystems
- Purpose: Update attached particle systems
- Calls: None

## Globals
- None

## Dependencies
- Common/DamageFX.h
- GameLogic/Module/BodyModule.h
- GameLogic/Damage.h
- GameLogic/Armor.h
- GameLogic/ArmorSet.h
