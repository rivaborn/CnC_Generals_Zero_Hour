# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BoneFXDamage.h

## Purpose
Defines the BoneFXDamage module for handling damage-related effects on bone animations in the SAGE engine.

## Responsibilities
- Extends DamageModule to handle damage events on bone animations
- Provides callbacks for damage, healing, and body damage state changes
- Manages memory allocation via custom memory pool glue
- Implements standard module macros for registration and serialization

## Key Types
- **BodyDamageType (Enum)**: Damage state type (forward-declared).
- **BoneFXDamage (Class)**: Damage module for bone animation effects.
- **BoneFXDamageMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **BoneFXDamage_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### BoneFXDamage::onBodyDamageStateChange
- Purpose: Handles transitions between body damage states.
- Calls: None visible in header.

### BoneFXDamage::onObjectCreated
- Purpose: Called when the associated object is created.
- Calls: None visible in header.

## Globals
None.

## Dependencies
- **DamageModule.h**: Base class for damage modules.
- **BodyDamageType**: Forward-declared enum from BodyModule.
