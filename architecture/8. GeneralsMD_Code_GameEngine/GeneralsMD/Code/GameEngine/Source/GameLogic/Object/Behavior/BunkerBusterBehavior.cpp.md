# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BunkerBusterBehavior.cpp

## Purpose
Implements the Bunker Buster behavior module that targets and damages garrisoned objects when the missile/bomb detonates.

## Responsibilities
- Handles missile/bomb behavior targeting garrisoned buildings
- Applies damage to occupants of targeted buildings
- Triggers visual and seismic effects on detonation
- Manages upgrade requirements for the weapon

## Key Types
- **BunkerBusterBehaviorModuleData (Class)**: Stores module configuration (FX, weapons, seismic settings)
- **BunkerBusterBehavior (Class)**: Implements the behavior logic and update cycle
- **DomeStyleSeismicFilter (Struct)**: Seismic effect filter (global instance)

## Key Functions
### `update`
- Purpose: Handles periodic updates and crash-through FX
- Calls: `getObject()`, `getAI()`, `getCurrentVictim()`, `testStatus()`, `FXList::doFXObj()`

### `onDie`
- Purpose: Triggered on missile/bomb death to initiate bunker busting
- Calls: `bustTheBunker()`

### `bustTheBunker`
- Purpose: Core logic for damaging garrisoned occupants and playing effects
- Calls: `findObjectByID()`, `getContain()`, `isBustable()`, `harmAndForceExitAllContained()`, `killAllContained()`, `FXList::doFXObj()`, `addSeismicSimulation()`, `createAndFireTempWeapon()`

### `xfer`
- Purpose: Serialization support
- Calls: `UpdateModule::xfer()`

## Globals
- **bunkerBusterHeavingEarthSeismicFilter (DomeStyleSeismicFilter)**: Global seismic filter for bunker buster effects

## Dependencies
- Key includes: `PreRTS.h`, `Common/Upgrade.h`, `GameLogic/Module/BunkerBusterBehavior.h`, `GameLogic/Module/ContainModule.h`, `GameLogic/GameLogic.h`, `GameClient/TerrainVisual.h`
- External symbols: `TheUpgradeCenter`, `TheGameLogic`, `TheTerrainVisual`, `TheWeaponStore`, `FXList`, `SeismicSimulationNode`
