# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/proxy.h

## Purpose
Defines a `ProxyClass` for storing a name and transformation matrix, likely used for scene object references in the 3D engine.

## Responsibilities
- Encapsulates a name and transformation matrix
- Provides equality comparison operators
- Offers getter/setter methods for name and transform

## Key Types
- **ProxyClass (Class)**: Stores a named 3D transform proxy.

## Key Functions
### ProxyClass::operator==
- Purpose: Compares two proxies for equality.
- Calls: None (inline comparison).

### ProxyClass::operator!=
- Purpose: Compares two proxies for inequality.
- Calls: None (inline comparison).

### ProxyClass::Get_Name
- Purpose: Returns the proxy's name.
- Calls: None.

### ProxyClass::Set_Name
- Purpose: Sets the proxy's name.
- Calls: None.

### ProxyClass::Get_Transform
- Purpose: Returns the proxy's transformation matrix.
- Calls: None.

### ProxyClass::Set_Transform
- Purpose: Sets the proxy's transformation matrix.
- Calls: None.

## Globals
- None.

## Dependencies
- `wwstring.h` (StringClass)
- `matrix3d.h` (Matrix3D)
