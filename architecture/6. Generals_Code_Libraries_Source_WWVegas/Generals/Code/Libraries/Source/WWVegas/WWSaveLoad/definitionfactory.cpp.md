# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionfactory.cpp

## Purpose
Implements the base class for definition factories used in the save/load system.

## Responsibilities
- Provides constructor/destructor for factory registration/unregistration
- Manages linked list pointers for factory chaining
- Registers/unregisters factories with the manager

## Key Types
- DefinitionFactoryClass (Class): base class for definition factories

## Key Functions
### DefinitionFactoryClass::DefinitionFactoryClass
- Purpose: Constructor that registers the factory with the manager
- Calls: DefinitionFactoryMgrClass::Register_Factory

### DefinitionFactoryClass::~DefinitionFactoryClass
- Purpose: Destructor that unregisters the factory from the manager
- Calls: DefinitionFactoryMgrClass::Unregister_Factory

## Globals
- None

## Dependencies
- definitionfactory.h
- definitionfactorymgr.h
- DefinitionFactoryMgrClass (external)
