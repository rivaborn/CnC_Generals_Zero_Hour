# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/wwsaveload.cpp

## Purpose
Implements the WWSaveLoad class for managing game save/load functionality and definition cleanup.

## Responsibilities
- Initializes and shuts down the save/load system
- Manages definition cleanup via DefinitionMgr
- Provides interface for save/load operations (stubs only)

## Key Types
- WWSaveLoad (Class): Core save/load manager

## Key Functions
### WWSaveLoad::Init
- Purpose: Initializes the save/load system
- Calls: None

### WWSaveLoad::Shutdown
- Purpose: Shuts down the save/load system and cleans up definitions
- Calls: _TheDefinitionMgr.Free_Definitions()

## Globals
- _TheDefinitionMgr (DefinitionMgr): Global definition manager instance

## Dependencies
- wwsaveload.h
- definitionmgr.h
- DefinitionMgr class (external)
