# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/persistfactory.cpp

## Purpose
Implements the PersistFactoryClass, which manages registration and unregistration of persistence factories in the save/load system.

## Responsibilities
- Registers/unregisters persistence factories with the SaveLoadSystem
- Provides base class for derived persistence factory implementations
- Manages linked list of factories via NextFactory pointer

## Key Types
- PersistFactoryClass (Class): Base class for persistence factory implementations

## Key Functions
### PersistFactoryClass()
- Purpose: Constructor that registers the factory with SaveLoadSystem
- Calls: SaveLoadSystemClass::Register_Persist_Factory

### ~PersistFactoryClass()
- Purpose: Destructor that unregisters the factory from SaveLoadSystem
- Calls: SaveLoadSystemClass::Unregister_Persist_Factory

## Globals
- None

## Dependencies
- persistfactory.h (header)
- saveload.h (SaveLoadSystemClass)
- SaveLoadSystemClass::Register_Persist_Factory
- SaveLoadSystemClass::Unregister_Persist_Factory
