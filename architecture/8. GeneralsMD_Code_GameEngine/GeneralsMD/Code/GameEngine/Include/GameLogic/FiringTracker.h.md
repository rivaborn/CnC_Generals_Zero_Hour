# GeneralsMD/Code/GameEngine/Include/GameLogic/FiringTracker.h

## Purpose
Header for the FiringTracker module, which tracks weapon firing history and manages cooldown states.

## Responsibilities
- Tracks shots fired by weapons
- Manages consecutive shot counts per victim
- Handles weapon cooldown and reload timing
- Provides audio feedback for looping sounds

## Key Types
- **FiringTrackerModuleData (Class)**: Module data container (empty)
- **FiringTracker (Class)**: Tracks firing history and cooldown logic
- **FiringTrackerMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **FiringTracker_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### FiringTracker::shotFired
- Purpose: Records a weapon shot at a victim
- Calls: None visible

### FiringTracker::update
- Purpose: Handles cooldown and reload timing
- Calls: speedUp, coolDown, calcTimeToSleep

### FiringTracker::getUpdatePhase
- Purpose: Returns PHASE_FINAL to ensure late execution
- Calls: None

### FiringTracker::speedUp
- Purpose: Increases object flag status for rapid firing
- Calls: None

### FiringTracker::coolDown
- Purpose: Slows down firing rate after inactivity
- Calls: None

### FiringTracker::calcTimeToSleep
- Purpose: Calculates sleep time based on cooldown
- Calls: None

## Globals
- None

## Dependencies
- Common/GameType.h
- Common/GameMemory.h
- Common/AudioEventRTS.h
- GameLogic/Module/UpdateModule.h
- Object, Weapon (forward declarations)
