# GeneralsMD/Code/GameEngine/Source/GameNetwork/IPEnumeration.cpp

## Purpose
Handles enumeration of local machine's IP addresses and hostname using Winsock.

## Responsibilities
- Initializes Winsock if needed
- Retrieves local machine's hostname and IP addresses
- Manages a linked list of enumerated IPs
- Cleans up Winsock resources on destruction

## Key Types
- `IPEnumeration` (Class): Manages IP address enumeration
- `EnumeratedIP` (Class): Represents a single IP address (defined elsewhere)

## Key Functions
### `IPEnumeration::IPEnumeration()`
- Purpose: Constructor initializes member variables
- Calls: None

### `IPEnumeration::~IPEnumeration()`
- Purpose: Destructor cleans up Winsock and IP list
- Calls: `WSACleanup()`, `deleteInstance()`

### `IPEnumeration::getAddresses()`
- Purpose: Retrieves and returns linked list of local IPs
- Calls: `WSAStartup()`, `gethostname()`, `gethostbyname()`, `newInstance()`

### `IPEnumeration::getMachineName()`
- Purpose: Retrieves local machine's hostname
- Calls: `WSAStartup()`, `gethostname()`

## Globals
None

## Dependencies
- `PreRTS.h`, `GameNetwork/IPEnumeration.h`
- Winsock API: `WSAStartup`, `WSACleanup`, `gethostname`, `gethostbyname`
- `DEBUG_LOG`, `AsciiString`, `UnsignedInt` (from engine)
- `EnumeratedIP` class (external)
