# Generals/Code/Libraries/Source/WWVegas/WWLib/rndstrng.cpp

## Purpose
Implements a random string selection utility class for the game.

## Responsibilities
- Manages a collection of strings.
- Provides random selection from the collection.
- Handles memory cleanup for stored strings.

## Key Types
- RandomStringClass (Class): Manages a list of strings and provides random selection.
- StringClass (Class): Represents individual strings (defined externally).

## Key Functions
### RandomStringClass::RandomStringClass
- Purpose: Default constructor for RandomStringClass.
- Calls: None.

### RandomStringClass::~RandomStringClass
- Purpose: Destructor that cleans up all stored strings.
- Calls: delete, Strings.Delete.

### RandomStringClass::Add_String
- Purpose: Adds a new string to the collection.
- Calls: W3DNEW, Strings.Add.

### RandomStringClass::Get_String
- Purpose: Returns a randomly selected string from the collection.
- Calls: Randomizer(), Strings.Count().

## Globals
None.

## Dependencies
- Key includes: "rndstrng.h", "wwstring.h"
- External symbols: Randomizer(), W3DNEW, StringClass, StringClass::operator*.
