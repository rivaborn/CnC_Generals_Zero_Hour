# Generals/Code/Libraries/Source/WWVegas/WWMath/Vector3i.h

## Purpose
Defines a 3D integer vector class for mathematical operations in the game engine.

## Responsibilities
- Stores 3D coordinates as integers (I, J, K)
- Provides equality comparison operators
- Supports array-style access to components

## Key Types
- Vector3i (Class): 3D integer vector with component access and comparison

## Key Functions
### Vector3i::Vector3i()
- Purpose: Default constructor
- Calls: None

### Vector3i::Vector3i(int i, int j, int k)
- Purpose: Parameterized constructor initializing components
- Calls: None

### Vector3i::operator==
- Purpose: Compares two vectors for equality
- Calls: None

### Vector3i::operator!=
- Purpose: Compares two vectors for inequality
- Calls: None

### Vector3i::operator[]
- Purpose: Provides array-style access to components
- Calls: None

## Globals
- None

## Dependencies
- "always.h" (for WWINLINE macro)
- Uses basic C++ types (int, bool)
