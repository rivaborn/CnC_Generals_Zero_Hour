# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crandom.h

## Purpose
Provides a random number generator class for game logic and effects.

## Responsibilities
- Generates random integers and floats
- Handles range-constrained random values
- Provides a global "free" random instance for unsynchronized effects

## Key Types
- CRandom (Class): Random number generator wrapper
- Random2Class (Class): Underlying generator (external)

## Key Functions
### CRandom::Get_Int()
- Purpose: Returns a random 32-bit integer
- Calls: Generator()

### CRandom::Get_Int(int max)
- Purpose: Returns a random integer less than max
- Calls: Generator()

### CRandom::Get_Int(int min, int max)
- Purpose: Returns a random integer in [min, max]
- Calls: Get_Int()

### CRandom::Get_Float()
- Purpose: Returns a random float in [0, 1]
- Calls: Get_Int()

### CRandom::Get_Float(float max)
- Purpose: Returns a random float in [0, max]
- Calls: Get_Float()

### CRandom::Get_Float(float min, float max)
- Purpose: Returns a random float in [min, max]
- Calls: Get_Float()

## Globals
- FreeRandom (CRandom): Global random instance for unsynchronized effects

## Dependencies
- `always.h`, `random.h`, `wwdebug.h`
- `Random2Class` (external generator)
