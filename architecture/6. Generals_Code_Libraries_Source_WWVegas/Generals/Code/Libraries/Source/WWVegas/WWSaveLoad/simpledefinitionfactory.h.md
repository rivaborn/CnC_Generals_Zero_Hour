# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/simpledefinitionfactory.h

## Purpose
Template class for creating simple definition factories in the SAGE engine.

## Responsibilities
- Provides a templated factory class for object creation
- Implements standard factory methods (Create, Get_Name, Get_Class_ID)
- Supports display toggling for factory objects
- Defines a macro for factory declaration

## Key Types
- SimpleDefinitionFactoryClass (Class): Templated factory class for creating definition objects

## Key Functions
### SimpleDefinitionFactoryClass::Create
- Purpose: Creates a new instance of the templated class
- Calls: W3DNEW

### SimpleDefinitionFactoryClass::Get_Name
- Purpose: Returns the name of the factory
- Calls: None

### SimpleDefinitionFactoryClass::Get_Class_ID
- Purpose: Returns the class ID of the factory
- Calls: None

## Globals
- DECLARE_DEFINITION_FACTORY (Macro): Macro for declaring factory instances

## Dependencies
- definitionfactory.h
- W3DNEW (memory allocation)
