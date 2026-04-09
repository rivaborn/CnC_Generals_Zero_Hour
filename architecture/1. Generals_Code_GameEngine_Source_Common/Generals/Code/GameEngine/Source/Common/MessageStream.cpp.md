# Generals/Code/GameEngine/Source/Common/MessageStream.cpp

## Purpose
This file implements the message stream and related classes for handling game messages in Command & Conquer Generals. It manages message creation, translation, and propagation.

## Responsibilities
- Manage game messages including their creation, arguments, and lifecycle.
- Handle message translators that process messages based on priority.
- Maintain a command list for processed messages.

## Key Types
- **GameMessage (Class)**: Represents a game message with various argument types.
- **CommandList (Class)**: Manages a list of commands to be executed.
- **TranslatorData (Struct)**: Holds data for attached translators, including priority and ID.

## Key Functions
### GameMessage::appendIntegerArgument
- Purpose: Appends an integer argument to the message.
- Calls: allocArg

### MessageStream::attachTranslator
- Purpose: Attaches a translator to the message stream with a specified priority.
- Calls: None

### MessageStream::propagateMessages
- Purpose: Propagates messages through attached translators and destroys them after processing.
- Calls: translateGameMessage, deleteInstance

## Globals
- **TheMessageStream (MessageStream \*)**: Singleton instance of the message stream.
- **TheCommandList (CommandList \*)**: Singleton instance of the command list.

## Dependencies
- Key includes:
  - "Common/MessageStream.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/Recorder.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/GameLogic.h"
