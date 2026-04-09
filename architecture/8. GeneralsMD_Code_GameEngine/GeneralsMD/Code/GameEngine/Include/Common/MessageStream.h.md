# GeneralsMD/Code/GameEngine/Include/Common/MessageStream.h

## Purpose
Defines the message system for the game engine, including message types, arguments, and the message stream/translator architecture.

## Responsibilities
- Defines game message types (input, commands, network messages)
- Provides message argument types and storage
- Implements message stream and translator system
- Manages command list for game logic execution

## Key Types
- GameMessage (Class): Base class for all game messages
- GameMessageArgument (Class): Stores message arguments of various types
- MessageStream (Class): Manages message propagation through translators
- CommandList (Class): Stores final commands for game logic execution
- GameMessageTranslator (Class): Interface for message translators

## Key Functions
### buildRegion
- Purpose: Constructs a valid 2D bounding region from anchor and destination points
- Calls: None

## Globals
- TheMessageStream (MessageStream*): Global message stream instance
- TheCommandList (CommandList*): Global command list instance

## Dependencies
- Common/GameCommon.h
- Common/SubsystemInterface.h
- Lib/BaseType.h
- Common/GameMemory.h
