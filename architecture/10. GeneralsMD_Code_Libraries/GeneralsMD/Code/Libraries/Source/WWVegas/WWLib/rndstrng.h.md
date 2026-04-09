# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rndstrng.h

## Purpose
Header file defining a random string selection utility class.

## Responsibilities
- Declares `RandomStringClass` for managing a pool of strings
- Provides methods to add and retrieve random strings
- Uses `DynamicVectorClass` for string storage and `Random2Class` for randomization

## Key Types
- `StringClass` (Class): Not inferable (forward declaration)
- `RandomStringClass` (Class): Manages a collection of strings and provides random selection

## Key Functions
### `Add_String`
- Purpose: Adds a string to the internal collection
- Calls: None

### `Get_String`
- Purpose: Returns a randomly selected string from the collection
- Calls: None

## Globals
- None

## Dependencies
- `vector.h` (for `DynamicVectorClass`)
- `random.h` (for `Random2Class`)
- `StringClass` (forward-declared)
