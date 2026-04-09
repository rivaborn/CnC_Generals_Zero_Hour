# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdinterface.cpp

## Purpose
Base class implementation for shader interfaces in the SAGE engine, managing shader definitions and references.

## Responsibilities
- Manages shader definition references via reference counting
- Provides access to shader definition data
- Handles construction/destruction of shader interface objects

## Key Types
- ShdInterfaceClass (Class): Base class for shader interfaces, holds definition pointer and class ID
- ShdDefClass (Class): Shader definition class (forward declared)

## Key Functions
### ShdInterfaceClass::ShdInterfaceClass
- Purpose: Constructor that initializes shader interface with definition and class ID
- Calls: REF_PTR_SET

### ShdInterfaceClass::~ShdInterfaceClass
- Purpose: Destructor that releases shader definition reference
- Calls: REF_PTR_RELEASE

### ShdInterfaceClass::Peek_Definition
- Purpose: Returns const pointer to shader definition
- Calls: None

## Globals
None

## Dependencies
- shdinterface.h: Header with class declarations
- shddef.h: Header for shader definition types
- REF_PTR_SET/REF_PTR_RELEASE: Reference counting macros (not shown in file)
