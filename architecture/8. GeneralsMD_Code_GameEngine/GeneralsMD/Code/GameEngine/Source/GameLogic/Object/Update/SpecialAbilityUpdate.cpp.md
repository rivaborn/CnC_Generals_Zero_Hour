# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SpecialAbilityUpdate.cpp

## Purpose
Handles processing of unit special abilities in the game, including preparation, triggering, and cleanup phases.

## Responsibilities
- Manages special ability states (approach, unpack, prepare, trigger, pack, finish)
- Handles persistent and non-target special abilities
- Validates and tracks special objects created by abilities
- Processes packing/unpacking animations and timing
- Cleans up resources when abilities complete or are aborted

## Key Types
- **SpecialAbilityUpdate (Class)**: Main class handling special ability logic
- **PackingState (Enum)**: Tracks packing/unpacking states (STATE_NONE, STATE_PACKING, STATE_UNPACKING)
- **SpecialPowerTemplate (Struct)**: Contains special power configuration data

## Key Functions
### update
- Purpose: Main update loop for special ability processing
- Calls: validateSpecialObjects, handlePackingProcessing, triggerAbilityEffect, continuePreparation, etc.

### triggerAbilityEffect
- Purpose: Executes the special ability effect when preparation is complete
- Calls: createSpecialObject, playAudioEvent, etc.

### handlePackingProcessing
- Purpose: Manages packing/unpacking animations and timing
- Calls: startPacking, endPacking, etc.

### validateSpecialObjects
- Purpose: Removes invalid special objects from tracking list
- Calls: TheGameLogic->findObjectByID

### finishAbility
- Purpose: Cleans up after ability completion
- Calls: ThePartitionManager->getClosestObject, ai->aiMoveToPosition

## Globals
- **TheGameLogic (GameLogic**)**: Global game logic instance
- **TheAudio (GameAudio**)**: Global audio system
- **ThePartitionManager (PartitionManager**)**: Global partition manager

## Dependencies
- Common: GameAudio, Player, SpecialPower, ThingFactory, ThingTemplate
- GameClient: Drawable, FXList, Eva, InGameUI, ControlBar, GameText
- GameLogic: AIPathfind, GameLogic, Object, PartitionManager, Weapon, ExperienceTracker
- GameLogic/Module: AIUpdate, LaserUpdate, PhysicsUpdate, SpecialAbilityUpdate, SpecialPowerModule, StickyBombUpdate, StealthUpdate, ContainModule
