# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/StructureBody.cpp

## Purpose
Implements the StructureBody class, which handles logic for structures in the game.

## Responsibilities
- Manages structure-specific behavior (construction, interaction).
- Tracks the constructor object that built the structure.
- Handles serialization (Xfer) and CRC for network sync.
- Extends ActiveBody functionality for structures.

## Key Types
- **StructureBody (Class)**: Manages structure behavior and state.
- **m_constructorObjectID (ObjectID)**: Stores the ID of the object that constructed this structure.

## Key Functions
### StructureBody::StructureBody
- Purpose: Constructor initializes StructureBody with a Thing and ModuleData.
- Calls: ActiveBody constructor.

### StructureBody::~StructureBody
- Purpose: Destructor (empty implementation).

### StructureBody::setConstructorObject
- Purpose: Sets the constructor object ID for this structure.
- Calls: None.

### StructureBody::crc
- Purpose: Generates/verifies CRC for network synchronization.
- Calls: ActiveBody::crc.

### StructureBody::xfer
- Purpose: Serializes/deserializes StructureBody state.
- Calls: ActiveBody::xfer, xfer->xferObjectID.

### StructureBody::loadPostProcess
- Purpose: Post-processing after loading (currently just calls parent).
- Calls: ActiveBody::loadPostProcess.

## Globals
- None.

## Dependencies
- **PreRTS.h**: Game engine precompiled header.
- **Common/Xfer.h**: Serialization utilities.
- **GameLogic/Object.h**: Base Object class.
- **GameLogic/Damage.h**: Damage-related logic.
- **GameLogic/Module/StructureBody.h**: Header for StructureBody.
