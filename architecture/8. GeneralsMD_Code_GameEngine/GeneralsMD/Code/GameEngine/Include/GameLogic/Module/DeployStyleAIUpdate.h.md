# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DeployStyleAIUpdate.h

## Purpose
Defines AI state machine for units that deploy/undeploy to switch between mobile and attack modes.

## Responsibilities
- Manages state transitions for deployable units
- Controls movement/attack restrictions based on deployment state
- Handles turret alignment and animation timing
- Provides configuration via module data

## Key Types
- DeployStateTypes (Enum): deployment states (READY_TO_MOVE, DEPLOY, READY_TO_ATTACK, UNDEPLOY, ALIGNING_TURRETS)
- DeployStyleAIUpdateModuleData (Class): configuration data for deployment behavior
- DeployStyleAIUpdate (Class): AI update module implementing deployment logic

## Key Functions
### DeployStyleAIUpdate::aiDoCommand
- Purpose: Handle AI commands based on current deployment state
- Calls: Not inferable

### DeployStyleAIUpdate::update
- Purpose: Update deployment state machine logic
- Calls: Not inferable

### DeployStyleAIUpdate::setMyState
- Purpose: Transition between deployment states
- Calls: Not inferable

## Globals
None

## Dependencies
- Common/StateMachine.h
- GameLogic/Module/AIUpdate.h
- INI parsing utilities (INI::parseDurationUnsignedInt, INI::parseBool)
