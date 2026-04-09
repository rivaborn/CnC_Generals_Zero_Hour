# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/PropagandaTowerBehavior.cpp

## Purpose
Implements the behavior module for Propaganda Towers in the game, handling scanning, influence effects, and state management.

## Responsibilities
- Manages scanning for objects within a radius
- Applies/removes influence effects (healing, weapon bonuses)
- Handles upgrade-dependent behavior
- Tracks objects under influence
- Manages state during capture, death, and construction

## Key Types
- **ObjectID (Enum)**: Identifier for game objects
- **ObjectTracker (Class)**: Tracks objects under influence (linked list node)
- **PropagandaTowerBehaviorModuleData (Class)**: Configuration data for the behavior
- **PropagandaTowerBehavior (Class)**: Main behavior module class

## Key Functions
### PropagandaTowerBehavior::update
- Purpose: Main update loop for scanning and applying effects
- Calls: doScan, effectLogic, removeAllInfluence, TheGameLogic->findObjectByID

### PropagandaTowerBehavior::doScan
- Purpose: Scans for objects in radius and updates influence list
- Calls: FXList::doFXObj, ThePartitionManager->iterateObjectsInRange, effectLogic

### PropagandaTowerBehavior::effectLogic
- Purpose: Applies/removes healing and weapon bonuses to objects
- Calls: obj->setWeaponBonusCondition, obj->clearWeaponBonusCondition, obj->attemptHealingFromSoleBenefactor

### PropagandaTowerBehavior::removeAllInfluence
- Purpose: Removes all effects from tracked objects
- Calls: effectLogic, TheGameLogic->findObjectByID

## Globals
- **TheUpgradeCenter (External)**: Upgrade management system
- **ThePlayerList (External)**: Player management system
- **TheGameLogic (External)**: Core game logic system
- **ThePartitionManager (External)**: Spatial partitioning system

## Dependencies
- Common/GameState.h, Common/Player.h, Common/PlayerList.h, Common/Upgrade.h
- GameClient/Drawable.h, GameClient/FXList.h
- GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/PartitionManager.h
- GameLogic/Module/PropagandaTowerBehavior.h, GameLogic/Module/BodyModule.h
