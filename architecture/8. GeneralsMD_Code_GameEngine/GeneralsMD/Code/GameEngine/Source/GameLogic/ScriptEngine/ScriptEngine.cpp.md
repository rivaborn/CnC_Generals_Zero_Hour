# GeneralsMD/Code/GameEngine/Source/GameLogic/ScriptEngine/ScriptEngine.cpp

## Purpose
Core scripting engine for Command & Conquer Generals/Zero Hour, handling game logic scripting, particle system management, and debugging tools.

## Responsibilities
- Execute game scripts and manage script actions/conditions
- Handle particle system creation, editing, and serialization
- Provide debugging interfaces and performance monitoring
- Manage attack priority information for AI targeting
- Support INI file parsing for game data

## Key Types
- **AttackPriorityInfo (Class)**: Manages attack priority settings for AI targeting
- **ScriptEngine (Class)**: Main game scripting engine
- **Template (Struct)**: Base template structure for script actions
- **K_SCRIPTS_DATA_VERSION_1 (Enum)**: Script data version constant
- **MAX_SPIN_COUNT (Enum)**: Maximum spin count constant

## Key Functions
### parseScriptAction
- Purpose: Parse script action definitions from INI files
- Calls: INI::initFromINI, TheScriptEngine->addActionTemplateInfo

### addActionTemplateInfo
- Purpose: Add/update script action template information
- Calls: None directly visible

### _writeSingleParticleSystem
- Purpose: Serialize particle system template to INI format
- Calls: File::write, various string formatting functions

### _updateAndSetCurrentSystem
- Purpose: Update and set current particle system in editor
- Calls: _getParticleSystemName, _addUpdatedParticleSystem, TheParticleSystemManager methods

### _reloadParticleSystemFromINI
- Purpose: Reload particle system from INI file
- Calls: File operations, INI loading, particle system update functions

## Globals
- **TheScriptEngine (ScriptEngine*)**: Global script engine instance
- **st_ParticleDLL (HMODULE)**: Handle to particle editor DLL
- **st_particleSystem (ParticleSystem*)**: Current particle system being edited
- **FRAMES_TO_SHOW_WIN_LOSE_MESSAGE (Int)**: Frames to display victory/defeat message
- **TheTemplateFieldParseTable (FieldParse[])**: Field parsing table for templates

## Dependencies
- Common game engine modules (DataChunk, File, GameEngine, etc.)
- GameLogic modules (ScriptActions, ScriptConditions, etc.)
- GameClient modules (MessageBox, Shell, View)
- W3D asset management
- INI parsing utilities
- Xfer serialization system
