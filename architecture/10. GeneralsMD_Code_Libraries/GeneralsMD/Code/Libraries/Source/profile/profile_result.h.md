# GeneralsMD/Code/Libraries/Source/profile/profile_result.h

## Purpose
Defines the abstract interface for profile result handlers in the SAGE engine.

## Responsibilities
- Declares the `ProfileResultInterface` abstract base class
- Defines pure virtual methods for writing results and cleanup
- Prevents copying of result instances
- Provides protected default constructor

## Key Types
- **ProfileResultInterface (Class)**: Abstract interface for profile result handlers

## Key Functions
### ProfileResultInterface()
- Purpose: Protected default constructor
- Calls: None

### WriteResults()
- Purpose: Pure virtual method to write profiling results on program exit
- Calls: None

### Delete()
- Purpose: Pure virtual method for safe deletion of result instances
- Calls: None

## Globals
- None

## Dependencies
- None (header-only, no external symbols)
