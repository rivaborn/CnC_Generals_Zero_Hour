# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/InactiveBody.cpp

## Purpose
Implements the InactiveBody module, which represents objects without health/damage mechanics, used for prerequisites or non-interactive entities.

## Responsibilities
- Handles damage/healing attempts (always returns 0 damage)
- Manages object death via DAMAGE_UNRESISTABLE
- Provides stub implementations for health-related functions
- Serializes/deserializes module state
- Marks object as "effectively dead" on creation

## Key Types
- **InactiveBody (class)**: Module for objects without health/damage
- **BodyDamageType (enum)**: Damage state (only BODY_PRISTINE used)

## Key Functions
### InactiveBody()
- Purpose: Constructor marks object as effectively dead
- Calls: getObject()->setEffectivelyDead()

### estimateDamage()
- Purpose: Returns 0 damage (except for DAMAGE_UNRESISTABLE)
- Calls: None

### attemptDamage()
- Purpose: Handles damage attempts (no effect except for DAMAGE_UNRESISTABLE)
- Calls: attemptHealing(), getObject()->onDie()

### attemptHealing()
- Purpose: Handles healing attempts (no effect)
- Calls: attemptDamage()

### getHealth()
- Purpose: Always returns 0.0f
- Calls: None

### xfer()
- Purpose: Serializes module state
- Calls: BodyModule::xfer()

## Globals
- **None**

## Dependencies
- Common/ThingTemplate.h
- Common/Xfer.h
- GameLogic/Module/InactiveBody.h
- GameLogic/Module/DieModule.h
- GameLogic/Damage.h
- GameLogic/GameLogic.h
- GameLogic/Object.h
