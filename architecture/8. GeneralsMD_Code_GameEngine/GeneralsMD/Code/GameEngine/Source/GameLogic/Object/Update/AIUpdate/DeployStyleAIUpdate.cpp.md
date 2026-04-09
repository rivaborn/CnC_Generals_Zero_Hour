# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/DeployStyleAIUpdate.cpp

## Purpose
Handles AI updates for units that must deploy to attack and pack before moving.

## Responsibilities
- Manages deployment/undeployment states for units
- Handles animation timing for deploy/undeploy sequences
- Controls turret alignment and weapon functionality
- Processes AI commands while respecting deployment constraints
- Plays deployment-related sound effects

## Key Types
- DeployStyleAIUpdate (Class): Manages deployment behavior for units
- DeployStateTypes (Enum): Represents deployment states (READY_TO_MOVE, READY_TO_ATTACK, DEPLOY, UNDEPLOY, ALIGNING_TURRETS)
- DeployStyleAIUpdateModuleData (Struct): Configuration data for deployment behavior

## Key Functions
### DeployStyleAIUpdate::update
- Purpose: Main update loop handling deployment state transitions
- Calls: getObject, getCurrentWeapon, TheGameLogic->getFrame, getDeployStyleAIUpdateModuleData, isWaitingForPath, getPath, getStateMachine->isInAttackState, getStateMachine->isInGuardIdleState, getAI, getCurrentVictim, getCurrentVictimPos, weapon->isWithinAttackRange, setMyState, getWhichTurretForCurWeapon, doTurretsHaveToCenterBeforePacking, setLocomotorGoalNone, AIUpdateInterface::update

### DeployStyleAIUpdate::setMyState
- Purpose: Transitions between deployment states and handles associated logic
- Calls: getObject, TheGameLogic->getFrame, getDeployStyleAIUpdateModuleData, getUnpackTime, getPackTime, getPerUnitSound, TheAudio->addAudioEvent, setTurretEnabled, recenterTurret

### DeployStyleAIUpdate::xfer
- Purpose: Serialization/deserialization for network sync
- Calls: AIUpdateInterface::xfer, xferVersion, xferUser, xferUnsignedInt, xferBool, xferObjectID, xferCoord3D, AICommandParmsStorage::doXfer

## Globals
- None

## Dependencies
- PreRTS.h, Common/Player.h, Common/ThingFactory.h, Common/ThingTemplate.h
- GameClient/Drawable.h, GameClient/InGameUI.h
- GameLogic/ExperienceTracker.h, GameLogic/Locomotor.h, GameLogic/Object.h, GameLogic/PartitionManager.h, GameLogic/Weapon.h
- GameLogic/Module/BodyModule.h, GameLogic/Module/ContainModule.h, GameLogic/Module/DeployStyleAIUpdate.h, GameLogic/Module/PhysicsUpdate.h
- TheGameLogic, TheAudio (external symbols)
