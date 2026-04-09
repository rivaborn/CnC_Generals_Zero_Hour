# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameMessageParser.cpp

## Purpose
Parses and structures game message arguments for efficient access.

## Responsibilities
- Constructs argument type lists from GameMessage objects
- Manages linked list of argument type descriptors
- Tracks counts of consecutive arguments of the same type
- Provides memory management for parser instances

## Key Types
- GameMessageParser (Class): main parser class managing argument type list
- GameMessageParserArgumentType (Class): node in linked list storing type and count
- GameMessageArgumentDataType (Enum): type identifier for message arguments

## Key Functions
### GameMessageParser::GameMessageParser(GameMessage *msg)
- Purpose: Initializes parser by analyzing message argument types
- Calls: getArgumentCount, getArgumentDataType, addArgType

### addArgType(GameMessageArgumentDataType type, Int argCount)
- Purpose: Adds a new argument type descriptor to the linked list
- Calls: newInstance (for GameMessageParserArgumentType)

### GameMessageParserArgumentType::GameMessageParserArgumentType(GameMessageArgumentDataType type, Int argCount)
- Purpose: Constructs an argument type descriptor node
- Calls: None

## Globals
- None

## Dependencies
- GameMessageParser.h (header)
- PreRTS.h (engine precompiled header)
- GameMessage class (from GameMessageParser.h)
- GameMessageArgumentDataType enum (from GameMessageParser.h)
- newInstance template function (memory management)
