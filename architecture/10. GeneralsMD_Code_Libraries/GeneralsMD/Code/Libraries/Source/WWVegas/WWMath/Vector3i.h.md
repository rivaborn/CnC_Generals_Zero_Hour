# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/Vector3i.h

## Purpose
Defines integer-based 3D vector classes for mathematical operations in the game engine.

## Responsibilities
- Provides `Vector3i` (32-bit int) and `Vector3i16` (16-bit unsigned int) classes
- Implements basic vector operations (construction, comparison, indexing)
- Supports array-style access to vector components

## Key Types
- **Vector3i (Class)**: 3D vector using 32-bit integers (I, J, K components)
- **Vector3i16 (Class)**: 3D vector using 16-bit unsigned integers (I, J, K components)

## Key Functions
### Vector3i::Vector3i(int i, int j, int k)
- Purpose: Constructs a 32-bit integer vector
- Calls: None

### Vector3i::operator==(const Vector3i &v)
- Purpose: Compares two vectors for equality
- Calls: None

### Vector3i::operator[](int n)
- Purpose: Provides array-style access to vector components
- Calls: None

### Vector3i16::Vector3i16(unsigned short i, unsigned short j, unsigned short k)
- Purpose: Constructs a 16-bit unsigned integer vector
- Calls: None

### Vector3i16::operator==(const Vector3i &v)
- Purpose: Compares a 16-bit vector with a 32-bit vector
- Calls: None

### Vector3i16::operator[](int n)
- Purpose: Provides array-style access to 16-bit vector components
- Calls: None

## Globals
None

## Dependencies
- `always.h` (for `
