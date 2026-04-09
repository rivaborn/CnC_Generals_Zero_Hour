# Generals/Code/Libraries/Source/WWVegas/WW3D2/proxy.h

## Purpose
Defines a `ProxyClass` for storing a name and transformation matrix, likely used for scene object references in the 3D engine.

## Responsibilities
- Stores a name and transformation matrix
- Provides equality comparison operators
- Offers getter/setter methods for name and transform

## Key Types
- **ProxyClass (Class)**: Wrapper for a named 3D transform (name + Matrix3D)

## Key Functions
### ProxyClass::operator==
- Purpose: Compares two ProxyClass instances for equality
- Calls: None (direct comparison of members)

### ProxyClass::operator!=
- Purpose: Compares two ProxyClass instances for inequality
- Calls: None (direct comparison of members)

## Globals
- None

## Dependencies
- `wwstring.h` (StringClass)
- `matrix3d.h` (Matrix3D)
