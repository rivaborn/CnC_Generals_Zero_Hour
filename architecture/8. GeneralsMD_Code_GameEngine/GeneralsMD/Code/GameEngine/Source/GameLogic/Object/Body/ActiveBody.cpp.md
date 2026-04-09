# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/ActiveBody.cpp

## Purpose
Manages health, damage, and state transitions for game objects with active bodies (units, structures, etc.).

## Responsibilities
- Tracks health, damage states, and armor
- Handles damage application and healing
- Manages particle effects for damage states
- Controls subdual mechanics and veterancy
- Serializes body state for networking

## Key Types
- **BodyParticleSystem (Class)**: Tracks particle effects tied to damage states
- **BodyParticleSystemMagicEnum (Enum)**: Not inferable
- **BodyParticleSystem_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### calcDamageState
- Purpose: Determines current damage state based on health ratio
- Calls: None

### ActiveBody::attemptDamage
- Purpose: Applies damage to the object after armor calculations
- Calls: validateArmorAndDamageFX, doDamageFX, internalChangeHealth, etc.

### ActiveBody::setCorrectDamageState
- Purpose: Updates visual/damage state based on current health
- Calls: calcDamageState, getObject, setGeometryInfoZ, etc.

## Globals
- **YELLOW_DAMAGE_PERCENT (float)**: Threshold for yellow damage warning (0.25f)

## Dependencies
- Common: BitFlagsIO, CRCDebug, DamageFX, Player, GameState, GlobalData, PlayerList, Team, Thing, ThingTemplate, Xfer
- GameClient: ControlBar, Drawable, InGameUI, ParticleSys
- GameLogic: AI, AIPathfind, Armor, GameLogic, Object, Damage, PartitionManager, TerrainLogic, Weapon
- GameLogic/Module: AIUpdate, ActiveBody, BridgeBehavior, ContainModule, DamageModule, DieModule
