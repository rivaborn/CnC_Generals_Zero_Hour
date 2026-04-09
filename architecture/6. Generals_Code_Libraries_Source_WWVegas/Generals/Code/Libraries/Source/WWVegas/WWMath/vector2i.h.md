# Generals/Code/Libraries/Source/WWVegas/WWMath/vector2i.h

## Purpose
Defines a 2D integer vector class for mathematical operations in the game engine.

## Responsibilities
- Stores 2D integer coordinates (I, J)
- Provides basic vector operations (construction, comparison, access)
- Supports element-wise swapping

## Key Types
- Vector2i (Class): 2D integer vector with coordinate access and comparison operators

## Key Functions
### Vector2i::Vector2i(int i, int j)
- Purpose: Constructs a Vector2i with specified coordinates
- Calls: None

### Vector2i::Set(int i, int j)
- Purpose: Sets the vector's coordinates
- Calls: None

### Vector2i::Swap(Vector2i & other)
- Purpose: Swaps contents with another Vector2i using XOR trick
- Calls: None

### Vector2i::operator==(const Vector2i & v)
- Purpose: Compares two vectors for equality
- Calls: None

### Vector2i::operator[] (int n)
- Purpose: Provides array-style access to vector components
- Calls: None

## Globals
None

## Dependencies
- "always.h" (for WWINLINE macro)
- Uses basic C++ types (int, bool)
