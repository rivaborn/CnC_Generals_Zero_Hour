# Generals/Code/GameEngine/Source/GameNetwork/User.cpp

## Purpose
Implements the User class for managing player network identities in the game.

## Responsibilities
- Constructs User objects with name, IP address, and port
- Provides comparison operators for User equality/inequality
- Allows modification of user name

## Key Types
- User (Class): Represents a networked player with name, IP, and port

## Key Functions
### User::User(UnicodeString, UnsignedInt, UnsignedInt)
- Purpose: Initializes a User with name, IP address, and port
- Calls: m_name.set()

### User::operator=(const User*)
- Purpose: Assigns values from another User to this one
- Calls: None

### User::operator==(const User*)
- Purpose: Compares two Users for equality based on name
- Calls: m_name.compare()

### User::operator!=(const User*)
- Purpose: Compares two Users for inequality based on name
- Calls: m_name.compare()

### User::setName(UnicodeString)
- Purpose: Updates the user's name
- Calls: m_name.set()

## Globals
- None

## Dependencies
- "PreRTS.h" (include)
- "GameNetwork/User.h" (include)
- UnicodeString, UnsignedInt, Bool (types)
