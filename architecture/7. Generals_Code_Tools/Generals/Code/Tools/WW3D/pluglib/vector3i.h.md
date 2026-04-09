# Generals/Code/Tools/WW3D/pluglib/vector3i.h

## Purpose
Defines a 3D integer vector class for mathematical operations in the WWMath library.

## Responsibilities
- Stores 3D coordinates as integers (I, J, K).
- Provides basic comparison and indexing operations.
- Supports inline construction and equality checks.

## Key Types
- **Vector3i (Class)**: Represents a 3D integer vector with I, J, K components.

## Key Functions
### Vector3i::Vector3i(void)
- Purpose: Default constructor for Vector3i.
- Calls: None.

### Vector3i::Vector3i(int i, int j, int k)
- Purpose: Constructs a Vector3i with specified integer components.
- Calls: None.

### Vector3i::operator==
- Purpose: Compares two Vector3i instances for equality.
- Calls: None.

### Vector3i::operator!=
- Purpose: Compares two Vector3i instances for inequality.
- Calls: None.

### Vector3i::operator[] (const)
- Purpose: Provides const access to vector components via array indexing.
- Calls: None.

### Vector3i::operator[] (non-const)
- Purpose: Provides non-const access to vector components via array indexing.
- Calls: None.

## Globals
- None.

## Dependencies
- Key includes: "always.h"
- External symbols: `WWINLINE` (macro for inline functions).
