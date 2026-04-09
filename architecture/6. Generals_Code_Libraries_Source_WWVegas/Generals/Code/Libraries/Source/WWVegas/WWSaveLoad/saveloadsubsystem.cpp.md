# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadsubsystem.cpp

## Purpose
Defines the base class for save/load subsystem registration in the SAGE engine.

## Responsibilities
- Provides base class for save/load subsystems
- Handles automatic registration with SaveLoadSystemClass
- Manages subsystem linking via NextSubSystem pointer

## Key Types
- SaveLoadSubSystemClass (Class): base class for save/load subsystems

## Key Functions
### SaveLoadSubSystemClass::SaveLoadSubSystemClass
- Purpose: Constructor that registers the subsystem with SaveLoadSystemClass
- Calls: SaveLoadSystemClass::Register_Sub_System

### SaveLoadSubSystemClass::~SaveLoadSubSystemClass
- Purpose: Destructor that unregisters the subsystem from SaveLoadSystemClass
- Calls: SaveLoadSystemClass::Unregister_Sub_System

## Globals
- None

## Dependencies
- saveloadsubsystem.h
- saveload.h
- SaveLoadSystemClass (external)
