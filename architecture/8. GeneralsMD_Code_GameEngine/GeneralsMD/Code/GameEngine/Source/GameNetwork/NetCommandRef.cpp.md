# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetCommandRef.cpp

## Purpose
Implements the NetCommandRef class, managing references to network command messages.

## Responsibilities
- Constructs and destroys NetCommandRef instances
- Attaches/detaches from network command messages
- Tracks reference counts for network commands
- Provides debug logging for reference tracking

## Key Types
- NetCommandRef (Class): reference-counted wrapper for network commands
- NetCommandMsg (Class): underlying network command message

## Key Functions
### NetCommandRef::NetCommandRef
- Purpose: Constructor that attaches to a network command message
- Calls: m_msg->attach()

### NetCommandRef::~NetCommandRef
- Purpose: Destructor that detaches from the network command message
- Calls: m_msg->detach()

## Globals
- refNum (UnsignedInt): debug counter for NetCommandRef instances

## Dependencies
- "GameNetwork/NetCommandRef.h"
- NetCommandMsg class
- DEBUG_LOG macro
- DEBUG_ASSERTCRASH macro
