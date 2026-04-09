# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/simpledefinitionfactory.h

## Purpose
Template class for creating simple definition factories in the SAGE engine.

## Responsibilities
- Provides a templated factory class for object creation
- Implements standard factory methods (Create, Get_Name, Get_Class_ID)
- Manages display visibility flag
- Generates factory instances via macro

## Key Types
- SimpleDefinitionFactoryClass (Class): Template factory for creating definition objects

## Key Functions
### SimpleDefinitionFactoryClass::Create
- Purpose: Creates a new instance of the template type T
- Calls: W3DNEW

### SimpleDefinitionFactoryClass::Get_Name
- Purpose: Returns the name string for the factory
- Calls: None

### SimpleDefinitionFactoryClass::Get_Class_ID
- Purpose: Returns the class ID for the factory
- Calls: None

## Globals
- DECLARE_DEFINITION_FACTORY (Macro): Generates factory instance and name string

## Dependencies
- definitionfactory.h
- W3DNEW (memory allocation)
- uint32 (type definition)
