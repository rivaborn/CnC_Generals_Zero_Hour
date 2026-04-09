# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameMessageParser.h

## Purpose
Defines classes for parsing game network messages and managing their argument types.

## Responsibilities
- Parses game messages into argument types
- Manages linked list of argument type descriptors
- Provides access to message argument metadata

## Key Types
- **GameMessageParserArgumentType (Class)**: Represents a single argument type in a message
- **GameMessageParserArgumentTypeMagicEnum (Enum)**: Not inferable (likely internal glue)
- **GameMessageParserArgumentType_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable
- **GameMessageParser (Class)**: Main parser class that manages a sequence of argument types
- **GameMessageParserMagicEnum (Enum)**: Not inferable
- **GameMessageParser_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### GameMessageParserArgumentType::GameMessageParserArgumentType
- Purpose: Constructs an argument type descriptor
- Calls: None

### GameMessageParser::GameMessageParser
- Purpose: Constructs a message parser (with/without a message)
- Calls: None

### GameMessageParser::addArgType
- Purpose: Adds an argument type to the parser's linked list
- Calls: None

## Globals
- None

## Dependencies
- `Common/MessageStream.h` (for GameMessage, GameMessageArgumentDataType)
- `Common/GameMemory.h` (for MemoryPoolObject)
- Memory pool management macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
