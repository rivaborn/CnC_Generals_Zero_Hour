# Generals/Code/Libraries/Source/WWVegas/WWLib/STRAW.H

## Purpose
Defines a base class for a demand-driven data carrier (Straw) that processes data through a chain of objects.

## Responsibilities
- Provides a virtual interface for data retrieval and chaining
- Manages pointers to next/previous objects in the chain
- Disables copying to enforce single ownership
- Serves as a base for derived classes that modify or monitor data

## Key Types
- Straw (Class): Base class for demand-driven data processing pipeline

## Key Functions
### Straw()
- Purpose: Default constructor initializing chain pointers to null
- Calls: None

### ~Straw()
- Purpose: Virtual destructor
- Calls: None

### Get_From(Straw*)
- Purpose: Sets the previous object in the chain
- Calls: None

### Get_From(Straw&)
- Purpose: Overload for reference-based chaining
- Calls: Get_From(Straw*)

### Get(void*, int)
- Purpose: Virtual method to retrieve data into a buffer
- Calls: None

## Globals
- None

## Dependencies
- None (header-only, no external symbols)
