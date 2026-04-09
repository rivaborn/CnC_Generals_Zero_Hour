# Generals/Code/GameEngine/Source/GameLogic/ScriptEngine/ScriptEngine.cpp

## Purpose
The ScriptEngine class interprets scripts for the Command & Conquer Generals game, handling various game logic and particle system management tasks.

## Responsibilities
- Interpreting and executing game scripts.
- Managing particle systems, including loading, updating, and rendering.
- Handling game state transitions and UI updates.
- Debugging and performance monitoring through integration with VTune.

## Key Types
- **AttackPriorityInfo (Class)**: Manages attack priorities for thing templates.
- **ScriptEngine (Class)**: Core class for script interpretation and game logic management.

## Key Functions
### ScriptEngine::ScriptEngine
- Purpose: Initializes the script engine, setting default values and states.
- Calls: None visible in this file.

### _appendMessage
- Purpose: Appends a message to the debug console or UI.
- Calls: None visible in this file.

### _updateFrameNumber
- Purpose: Updates the current frame number for game logic processing.
- Calls: None visible in this file.

### _addUpdatedParticleSystem
- Purpose: Adds an updated particle system to the manager.
- Calls: None visible in this file.

### _writeSingleParticleSystem
- Purpose: Writes a single particle system's configuration to an output stream.
- Calls: Various internal functions for appending parameters.

## Globals
- **st_LastCurrentFrame (int)**: Tracks the last processed frame number.
- **st_CurrentFrame (int)**: Tracks the current frame number.
- **st_CanAppCont (Bool)**: Indicates if the application can continue processing.
- **st_AppIsFast (Bool)**: Indicates if the application is running in fast mode.
- **TheScriptEngine (ScriptEngine*)**: Singleton instance of the script engine.

## Dependencies
- Key includes:
  - "common/DataChunk.h"
  - "Common/File.h"
  - "Common/FileSystem.h"
  - "Common/GameEngine.h"
  - "GameLogic/ScriptEngine.h"
  - "GameClient/ParticleSys.h"
  - "GameLogic/PartitionManager.h"
- External symbols:
  - Functions from `vtuneapi.dll` for performance monitoring.
  - Particle system management functions from external DLLs.
