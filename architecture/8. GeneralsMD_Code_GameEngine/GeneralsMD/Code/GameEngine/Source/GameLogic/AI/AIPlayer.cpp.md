# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIPlayer.cpp

## Purpose
Manages AI player behavior, including unit production, base management, and strategic decision-making.

## Responsibilities
- Controls AI player's building and unit production queues
- Manages supply chain and resource gathering
- Handles base defense and expansion logic
- Coordinates team formations and reinforcements
- Processes structure completion events

## Key Types
- **AIPlayer (Class)**: Main AI controller for a player
- **TeamInQueue (Class)**: Represents a team being built in the production queue
- **WorkOrder (Class)**: Individual production order within a team
- **BuildListInfo (External)**: Building production information

## Key Functions
### deleteQueue
- Purpose: Clears the production queue for a specific team
- Calls: `WorkOrder::deleteInstance`, `TeamInQueue::deleteInstance`

### onStructureProduced
- Purpose: Handles completion of a structure being built
- Calls: `BuildListInfo::setUnderConstruction`, `Object::updateObjValuesFromMapProperties`, `TheScriptEngine::runObjectScript`

### checkForSupplyCenter
- Purpose: Determines supply truck requirements for a completed supply center
- Calls: `SupplyCenterDockUpdate` methods, `TheAI->getAiData`

### queueSupplyTruck
- Purpose: Adds a supply truck to the production queue if needed
- Calls: `WorkOrder::newInstance`, `Object::getAI`, `SupplyTruckAIInterface` methods

## Globals
- **SUPPLY_CENTER_CLOSE_DIST (const)**: Distance threshold for supply center proximity checks
- **USE_DOZER (const)**: Flag for dozer (construction unit) usage

## Dependencies
- GameLogic headers (AI, GameLogic, Object)
- Common game systems (Player, Team, BuildAssistant)
- Scripting and template systems (ScriptEngine, ThingFactory)
- Partition management (PartitionManager)
- Networking/Xfer for save/load functionality
