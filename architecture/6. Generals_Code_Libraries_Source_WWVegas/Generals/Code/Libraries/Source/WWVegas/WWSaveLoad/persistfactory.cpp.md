# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/persistfactory.cpp

## Purpose
Implements the PersistFactoryClass, which manages registration and unregistration of persistence factories in the save/load system.

## Responsibilities
- Registers/unregisters persistence factories with the SaveLoadSystem
- Provides base class for derived persistence factory implementations
- Manages linked list of factories via NextFactory pointer

## Key Types
- PersistFactoryClass (Class): Base class for persistence factory implementations

## Key Functions
### PersistFactoryClass::PersistFactoryClass
- Purpose: Constructor that registers the factory with the SaveLoadSystem
- Calls: SaveLoadSystemClass::Register_Persist_Factory

### PersistFactoryClass::~PersistFactoryClass
- Purpose: Destructor that unregisters the factory from the SaveLoadSystem
- Calls: SaveLoadSystemClass::Unregister_Persist_Factory

## Globals
- None

## Dependencies
- persistfactory.h (header)
- saveload.h (header)
- SaveLoadSystemClass (external class)
- Register_Persist_Factory (external function)
- Unregister_Persist_Factory (external function)
