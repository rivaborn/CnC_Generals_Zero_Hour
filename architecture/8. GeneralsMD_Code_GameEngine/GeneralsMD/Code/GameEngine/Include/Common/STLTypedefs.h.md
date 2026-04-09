# GeneralsMD/Code/GameEngine/Include/Common/STLTypedefs.h

## Purpose
Defines STL-related typedefs and custom functors for the game engine.

## Responsibilities
- Provides STL container typedefs for game objects and data structures
- Defines custom hash and comparison functors for use with STL containers
- Forward declares core game types (Object, NameKeyType, etc.)

## Key Types
- **STLSpecialAlloc (Class)**: Custom memory allocator for STL containers
- **Object (Class)**: Base game object type
- **NameKeyType (Enum)**: Key type for named objects
- **ObjectID (Enum)**: Unique identifier for game objects
- **DrawableID (Enum)**: Identifier for drawable objects
- **AsciiStringList (typedef)**: List of AsciiString objects
- **ObjectPointerList (typedef)**: List of Object pointers
- **VecCoord3D (typedef)**: Vector of 3D coordinates
- **PosRequest (typedef)**: Pair of 2D and 3D coordinates
- **NamedRequest (typedef)**: Pair of AsciiString and Object pointer
- **BoolVector (typedef)**: Vector of boolean values
- **ProductionChangeMap (typedef)**: Map for production changes
- **ProductionVeterancyMap (typedef)**: Map for production veterancy levels
- **rts::hash (template)**: Generic hash functor
- **rts::equal_to (template)**: Generic equality comparison functor
- **rts::less_than_nocase (template)**: Case-insensitive less-than comparison functor

## Key Functions
### rts::hash<T>::operator()
- Purpose: Computes hash value for type T
- Calls: std::hash<T>::operator()

### rts::equal_to<T>::operator()
- Purpose: Compares two values of type T for equality
- Calls: None (uses operator==)

### rts::less_than_nocase<T>::operator()
- Purpose: Performs case-insensitive less-than comparison
- Calls: None (uses compareNoCase for strings)

## Globals
- **_STLP_USE_NEWALLOC (define)**: Enables custom STL allocator
- **STLSpecialAlloc (class)**: Forward declaration of custom allocator

## Dependencies
- Common/AsciiString.h
- Common/UnicodeString.h
- Common/GameCommon.h
- Common/GameMemory.h
- <algorithm>, <bitset>, <hash_map>, <list>, <map>, <queue>, <set>, <stack>, <string>, <vector>
