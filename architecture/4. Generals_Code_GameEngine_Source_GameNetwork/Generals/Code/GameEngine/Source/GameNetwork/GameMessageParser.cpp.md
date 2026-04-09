# Generals/Code/GameEngine/Source/GameNetwork/GameMessageParser.cpp

## Purpose
Parses and structures game message arguments for efficient access.

## Responsibilities
- Constructs argument type lists from GameMessage objects
- Manages linked list of argument type descriptors
- Tracks counts of consecutive arguments of the same type
- Provides memory management for parser state

## Key Types
- GameMessageParser (Class): main parser class that builds argument type lists
- GameMessageParserArgumentType (Class): linked list node storing type and count info

## Key Functions
### GameMessageParser::GameMessageParser(GameMessage *msg)
- Purpose: Initializes parser by analyzing message argument types
- Calls: addArgType

### GameMessageParser::addArgType
- Purpose: Adds a new argument type descriptor to the linked list
- Calls: newInstance (GameMessageParserArgumentType constructor)

## Globals
None

## Dependencies
- GameNetwork/GameMessageParser.h (header)
- PreRTS.h (engine precompiled header)
- GameMessage class (external)
- GameMessageArgumentDataType enum (external)
- newInstance template (memory management)
