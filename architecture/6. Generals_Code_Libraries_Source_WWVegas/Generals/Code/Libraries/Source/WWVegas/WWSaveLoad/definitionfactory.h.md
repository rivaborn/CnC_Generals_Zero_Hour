# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionfactory.h

## Purpose
Defines the abstract base class for definition factories, which act as virtual constructors for game object definitions.

## Responsibilities
- Declares the `DefinitionFactoryClass` interface
- Defines pure virtual methods for creating definitions and querying metadata
- Manages factory linking via `m_NextFactory` and `m_PrevFactory`

## Key Types
- **DefinitionFactoryClass (Class)**: Abstract base class for definition factories.
- **DefinitionClass (Class)**: Forward-declared base class for game definitions.

## Key Functions
### DefinitionFactoryClass::Create
- Purpose: Pure virtual method to create a new definition instance.
- Calls: None (pure virtual).

### DefinitionFactoryClass::Get_Name
- Purpose: Pure virtual method to retrieve the factory's name.
- Calls: None (pure virtual).

### DefinitionFactoryClass::Get_Class_ID
- Purpose: Pure virtual method to retrieve the factory's class ID.
- Calls: None (pure virtual).

### DefinitionFactoryClass::Is_Displayed
- Purpose: Pure virtual method to check if the factory should be displayed in UI.
- Calls: None (pure virtual).

## Globals
- None.

## Dependencies
- `always.h`, `bittype.h`, `definitionclassids.h`
- `DefinitionClass` (forward-declared)
- `DefinitionFactoryMgrClass` (friend class)
