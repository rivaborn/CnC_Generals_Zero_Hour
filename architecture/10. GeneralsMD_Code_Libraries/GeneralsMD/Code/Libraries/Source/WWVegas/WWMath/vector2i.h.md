# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vector2i.h

## Purpose
Defines a 2D integer vector class for mathematical operations in the game engine.

## Responsibilities
- Stores 2D integer coordinates (I, J)
- Provides basic vector operations (construction, assignment, comparison)
- Supports element access via array notation
- Implements efficient swap operation using XOR trick

## Key Types
- Vector2i (Class): 2D integer vector with coordinate storage and basic operations

## Key Functions
### Vector2i::Vector2i()
- Purpose: Default constructor initializing to (0, 0)
- Calls: None

### Vector2i::Vector2i(int i, int j)
- Purpose: Parameterized constructor setting initial coordinates
- Calls: None

### Vector2i::Set(int i, int j)
- Purpose: Sets the vector coordinates
- Calls: None

### Vector2i::Swap(Vector2i & other)
- Purpose: Swaps contents with another vector using XOR trick
- Calls: None

### Vector2i::operator==/operator!= (const Vector2i & v)
- Purpose: Equality/inequality comparison operators
- Calls: None

### Vector2i::operator[] (int n)
- Purpose: Array-style access to vector components
- Calls: None

## Globals
None

## Dependencies
- "always.h" (for WWINLINE macro)
- Uses basic C++ types (int, bool)
