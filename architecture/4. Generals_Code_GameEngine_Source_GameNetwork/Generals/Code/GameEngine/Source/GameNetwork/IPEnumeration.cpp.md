# Generals/Code/GameEngine/Source/GameNetwork/IPEnumeration.cpp

## Purpose
Handles enumeration of local machine's IP addresses using Winsock.

## Responsibilities
- Initializes Winsock if needed
- Retrieves host name and IP addresses via `gethostbyname`
- Maintains a sorted linked list of `EnumeratedIP` objects
- Cleans up Winsock and memory on destruction

## Key Types
- `IPEnumeration` (Class): Manages IP address enumeration
- `EnumeratedIP` (Class): Represents a single IP address (defined elsewhere)

## Key Functions
### `IPEnumeration::getAddresses`
- Purpose: Retrieves and returns a linked list of local IP addresses
- Calls: `WSAStartup`, `gethostname`, `gethostbyname`, `newInstance`, `DEBUG_LOG`

### `IPEnumeration::getMachineName`
- Purpose: Retrieves the local machine's host name
- Calls: `WSAStartup`, `gethostname`, `DEBUG_LOG`

## Globals
- `m_IPlist` (EnumeratedIP*): Head of the IP address linked list
- `m_isWinsockInitialized` (bool): Tracks Winsock initialization state

## Dependencies
- `PreRTS.h`, `GameNetwork/IPEnumeration.h`
- Winsock API (`WSAStartup`, `WSACleanup`, `gethostname`, `gethostbyname`)
- `DEBUG_LOG` macro
- `AsciiString` class
- `newInstance` template function
