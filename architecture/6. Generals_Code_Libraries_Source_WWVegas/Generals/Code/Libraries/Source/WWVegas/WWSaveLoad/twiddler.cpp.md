# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/twiddler.cpp

## Purpose
Implements the TwiddlerClass, a definition-based random object selector for the SAGE engine's save/load system.

## Responsibilities
- Manages a list of definition IDs for random selection
- Provides Twiddle() to randomly pick a definition
- Handles save/load persistence for Twiddler objects
- Supports indirect class creation via selected definitions

## Key Types
- TwiddlerClass (Class): Core class for random definition selection
- (anonymous enum) (Enum): Chunk IDs for save/load (CHUNKID_VARIABLES, CHUNKID_BASE_CLASS)
- (anonymous enum) (Enum): Variable IDs for micro-chunks (VARID_DEFINTION_ID, VARID_INDIRECT_CLASSID)

## Key Functions
### Twiddle
- Purpose: Randomly selects and returns a definition from the internal list
- Calls: RandomClass constructor, RandomClass operator()

### Create
- Purpose: Creates an instance of a randomly selected definition
- Calls: Twiddle(), DefinitionClass::Create()

### Save
- Purpose: Saves Twiddler state to a chunk save stream
- Calls: ChunkSaveClass::Begin_Chunk/End_Chunk, Save_Variables, DefinitionClass::Save

### Load
- Purpose: Loads Twiddler state from a chunk load stream
- Calls: ChunkLoadClass::Open_Chunk/Close_Chunk/Cur_Chunk_ID, Load_Variables, DefinitionClass::Load

### Save_Variables
- Purpose: Serializes definition list and indirect class ID
- Calls: WRITE_MICRO_CHUNK macro

### Load_Variables
- Purpose: Deserializes definition list and indirect class ID
- Calls: ChunkLoadClass::Open_Micro_Chunk/Close_Micro_Chunk/Cur_Micro_Chunk_ID/Read, READ_MICRO_CHUNK macro

## Globals
- _TwiddlerFactory (DefinitionFactoryClass): Factory for TwiddlerClass definitions
- _TwiddlerPersistFactory (SimplePersistFactoryClass): Persistence factory for TwiddlerClass

## Dependencies
- twiddler.h, random.h, saveloadids.h, simpledefinitionfactory.h, persistfactory.h, win.h, wwhack.h
- DefinitionMgrClass, ChunkSaveClass, ChunkLoadClass, DefinitionClass, PersistClass, PersistFactoryClass
