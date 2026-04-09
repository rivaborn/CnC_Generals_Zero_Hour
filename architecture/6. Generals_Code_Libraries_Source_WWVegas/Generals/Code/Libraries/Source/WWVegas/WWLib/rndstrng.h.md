# Generals/Code/Libraries/Source/WWVegas/WWLib/rndstrng.h

## Purpose
Header file defining a random string selection utility class.

## Responsibilities
- Manages a collection of strings
- Provides random string selection
- Supports adding strings to the collection

## Key Types
- **StringClass (Class)**: Not inferable (forward declaration).
- **RandomStringClass (Class)**: Manages a pool of strings and selects one randomly.
- **DynamicVectorClass<StringClass*> (Type)**: Container for storing string pointers.
- **Random2Class (Type)**: Random number generator for string selection.

## Key Functions
### RandomStringClass()
- Purpose: Constructor initializes the random string manager.
- Calls: Not inferable.

### ~RandomStringClass()
- Purpose: Destructor cleans up the random string manager.
- Calls: Not inferable.

### Add_String(const char *str)
- Purpose: Adds a string to the pool for random selection.
- Calls: Not inferable.

### Get_String()
- Purpose: Returns a randomly selected string from the pool.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- **vector.h**: For `DynamicVectorClass`.
- **random.h**: For `Random2Class`.
- **StringClass**: Forward-declared class for string storage.
