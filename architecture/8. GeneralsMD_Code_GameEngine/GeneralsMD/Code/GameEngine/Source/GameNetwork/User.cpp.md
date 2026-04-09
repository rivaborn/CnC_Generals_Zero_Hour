# GeneralsMD/Code/GameEngine/Source/GameNetwork/User.cpp

## Purpose
Implements the User class for network user representation, including construction, assignment, and comparison operations.

## Responsibilities
- Constructs User objects with name, IP address, and port
- Implements assignment and comparison operators
- Provides name modification functionality

## Key Types
- User (Class): Represents a network user with name, IP, and port

## Key Functions
### User::User
- Purpose: Constructs a User with specified name, address, and port
- Calls: m_name.set()

### User::operator=
- Purpose: Assigns values from another User to this one
- Calls: None

### User::operator==
- Purpose: Compares two Users for equality based on name
- Calls: m_name.compare()

### User::operator!=
- Purpose: Compares two Users for inequality based on name
- Calls: m_name.compare()

### User::setName
- Purpose: Updates the user's name
- Calls: m_name.set()

## Globals
None

## Dependencies
- "PreRTS.h"
- "GameNetwork/User.h"
- UnicodeString, UnsignedInt, Bool types
