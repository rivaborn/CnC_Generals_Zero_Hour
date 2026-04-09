# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/BattlePlanUpdate.cpp

## Purpose
Handles battle plan execution and state transitions for strategy center buildings in Command & Conquer Generals.

## Responsibilities
- Manages three battle plans: Bombardment, Hold the Line, and Search & Destroy
- Handles state transitions between plans with animations and sound effects
- Applies bonuses/penalties to units based on active plan
- Manages turret behavior during bombardment mode
- Handles vision object creation for Search & Destroy

## Key Types
- **BattlePlanUpdateModuleData (struct)**: Configuration data for battle plans
- **BattlePlanUpdate (class)**: Main update module handling plan execution
- **BattlePlanBonuses (struct)**: Contains bonuses applied to units
- **BattlePlanStatus (enum)**: PLANSTATUS_NONE, BOMBARDMENT, HOLDTHELINE, SEARCHANDDESTROY
- **TransitionStatus (enum)**: TRANSITIONSTATUS_IDLE, UNPACKING, ACTIVE, PACKING

## Key Functions
### update
- Purpose: Main update loop handling state transitions and plan execution
- Calls: setStatus, enableTurret, recenterTurret, setBattlePlan, TheAudio->addAudioEvent, TheInGameUI->message

### setBattlePlan
- Purpose: Applies or removes battle plan bonuses to player's army
- Calls: player->changeBattlePlan, body->setMaxHealth, obj->setVisionRange, obj->setShroudClearingRange, update->setSDEnabled, player->iterateObjects

### paralyzeTroop (static)
- Purpose: Callback for paralyzing troops when battle plan changes
- Calls: obj->setDisabledUntil

## Globals
- None

## Dependencies
- Common: BitFlagsIO, Radar, PlayerList, ThingTemplate, ThingFactory, Player, Xfer
- GameClient: GameClient, Drawable, GameText, ParticleSys, FXList, ControlBar
- GameLogic: GameLogic, PartitionManager, Object, ObjectIter, Weaponset, Weapon, TerrainLogic
- Modules: SpecialPowerModule, BattlePlanUpdate, PhysicsUpdate, ActiveBody, AIUpdate, StealthDetectorUpdate
