# GeneralsMD/Code/GameEngine/Source/Common/MessageStream.cpp

## Purpose
Implements the message stream system for handling game events and commands in the SAGE engine.

## Responsibilities
- Manages `GameMessage` creation, storage, and propagation
- Handles message translators for routing messages to appropriate systems
- Mainages the command list for deferred message processing
- Provides utility functions for message argument handling
- Supports debug/multiplayer command validation

## Key Types
- `GameMessage` (Class): Represents a game event/command with arguments
- `GameMessageArgument` (Struct): Holds typed message arguments
- `MessageStream` (Class): Manages the message stream and translators
- `CommandList` (Class): Stores commands for deferred processing
- `TranslatorData` (Struct): Internal translator registration data

## Key Functions
### `buildRegion`
- Purpose: Creates a 2D bounding region from two points
- Calls: None

### `MessageStream::propagateMessages`
- Purpose: Routes messages through attached translators and clears the stream
- Calls: `isInvalidDebugCommand`, `translateGameMessage`, `appendMessageList`

### `GameMessage::append*Argument`
- Purpose: Adds typed arguments to a message
- Calls: `allocArg`

## Globals
- `TheMessageStream` (MessageStream*): Singleton message stream instance
- `TheCommandList` (CommandList*): Singleton command list instance

## Dependencies
- `MessageStream.h`, `Player.h`, `PlayerList.h`, `Recorder.h`
- `InGameUI.h`, `GameLogic.h`
- `GameMessageTranslator`, `GameMessageList` (base classes)
