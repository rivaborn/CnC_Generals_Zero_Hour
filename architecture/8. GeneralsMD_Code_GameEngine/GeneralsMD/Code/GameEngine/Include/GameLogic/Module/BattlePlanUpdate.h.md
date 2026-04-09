# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BattlePlanUpdate.h

## Purpose
Defines the BattlePlanUpdate module for handling building states and battle plan execution in Command & Conquer Generals.

## Responsibilities
- Manages battle plan transitions (unpacking/packing)
- Applies bonuses based on active battle plans
- Handles special power execution for buildings
- Controls turret behavior and vision objects

## Key Types
- **BattlePlanUpdateModuleData (Class)**: Module configuration data
- **TransitionStatus (Enum)**: States for battle plan transitions
- **BattlePlanStatus (Enum)**: Types of battle plans
- **BattlePlanBonuses (Class)**: Stores bonuses applied by battle plans
- **BattlePlanUpdate (Class)**: Main update module for battle plans

## Key Functions
### BattlePlanUpdate::initiateIntentToDoSpecialPower
- Purpose: Initiates a special power action
- Calls: Not inferable

### BattlePlanUpdate::update
- Purpose: Handles periodic updates for battle plan state
- Calls: Not inferable

### BattlePlanUpdate::getActiveBattlePlan
- Purpose: Returns the currently active battle plan
- Calls: Not inferable

## Globals
- **ALL_PLANS (Int)**: Constant for plan stacking/removal

## Dependencies
- SpecialPowerUpdateModule.h
- Common/KindOf.h
- MemoryPoolObject (base class)
- MultiIniFieldParse (for parsing)
- Various forward-declared classes (SpecialPowerModule, ParticleSystem, etc.)
