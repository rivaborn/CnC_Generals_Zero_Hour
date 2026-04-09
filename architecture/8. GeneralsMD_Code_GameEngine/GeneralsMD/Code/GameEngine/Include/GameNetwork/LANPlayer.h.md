# GeneralsMD/Code/GameEngine/Include/GameNetwork/LANPlayer.h

## Purpose
Defines the LANPlayer class representing players in a LAN lobby, identified by IP addresses.

## Responsibilities
- Stores player metadata (name, login, host)
- Tracks last heard timestamp for timeout detection
- Manages linked list structure for player lists
- Provides IP address storage and access

## Key Types
- **LANPlayer (Class)**: Represents a LAN player with name, login, host, timestamp, linked list pointer, and IP.

## Key Functions
### LANPlayer()
- Purpose: Default constructor initializing all fields.
- Calls: None.

### getName()
- Purpose: Returns the player's name.
- Calls: None.

### setName()
- Purpose: Sets the player's name.
- Calls: None.

### getLogin()
- Purpose: Returns the player's login name.
- Calls: None.

### setLogin()
- Purpose: Sets the player's login name (Unicode or ASCII).
- Calls: None.

### getHost()
- Purpose: Returns the player's host machine name.
- Calls: None.

### setHost()
- Purpose: Sets the player's host machine name (Unicode or ASCII).
- Calls: None.

### getLastHeard()
- Purpose: Returns the last heard timestamp.
- Calls: None.

### setLastHeard()
- Purpose: Sets the last heard timestamp.
- Calls: None.

### getNext()
- Purpose: Returns the next player in the linked list.
- Calls: None.

### setNext()
- Purpose: Sets the next player in the linked list.
- Calls: None.

### getIP()
- Purpose: Returns the player's IP address.
- Calls: None.

### setIP()
- Purpose: Sets the player's IP address.
- Calls: None.

## Globals
- None.

## Dependencies
