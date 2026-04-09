# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadsubsystem.cpp

## Purpose
Defines the base class for save/load subsystem registration in the SAGE engine.

## Responsibilities
- Provides constructor/destructor for subsystem lifecycle
- Registers/unregisters subsystems with the global SaveLoadSystem
- Serves as parent class for specialized save/load handlers

## Key Types
- SaveLoadSubSystemClass (Class): abstract base for save/load subsystems

## Key Functions
### SaveLoadSubSystemClass()
- Purpose: Constructor that auto-registers the subsystem
- Calls: SaveLoadSystemClass::Register_Sub_System

### ~SaveLoadSubSystemClass()
- Purpose: Destructor that unregisters the subsystem
- Calls: SaveLoadSystemClass::Unregister_Sub_System

## Globals
- NextSubSystem (SaveLoadSubSystemClass*): linked list pointer for subsystem chaining

## Dependencies
- saveloadsubsystem.h (header)
- saveload.h (SaveLoadSystemClass)
- SaveLoadSystemClass::Register_Sub_System
- SaveLoadSystemClass::Unregister_Sub_System
