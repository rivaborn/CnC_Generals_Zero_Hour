# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rndstrng.cpp

## Purpose
Implements a random string selection utility class for the game.

## Responsibilities
- Manages a collection of strings
- Provides random selection from the collection
- Handles empty collection cases

## Key Types
- RandomStringClass (Class): manages random string selection
- Strings (WWStringArray): internal storage for strings

## Key Functions
### Add_String
- Purpose: Adds a string to the internal collection
- Calls: Strings.Add

### Get_String
- Purpose: Returns a random string from the collection
- Calls: Strings.Count, Randomizer

## Globals
None

## Dependencies
- rndstrng.h (header)
- wwstring.h (WWStringArray)
- Randomizer() (external random number generator)
