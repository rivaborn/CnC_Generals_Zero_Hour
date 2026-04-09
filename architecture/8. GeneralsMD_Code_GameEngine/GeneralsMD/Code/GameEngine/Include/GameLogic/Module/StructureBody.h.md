# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StructureBody.h

## Purpose
Defines the `StructureBody` class, a specialized `ActiveBody` for structures that are built and interactable by players.

## Responsibilities
- Extends `ActiveBody` for structure-specific behavior
- Manages construction object tracking
- Provides module data parsing
- Handles memory allocation via custom macros

## Key Types
- **StructureBodyModuleData (Class)**: Module data for `StructureBody`, extends `ActiveBodyModuleData`
- **StructureBody (Class)**: Main structure body class, extends `ActiveBody`
- **StructureBodyMagicEnum (Enum)**: Not inferable (empty enum)
- **StructureBody_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### StructureBodyModuleData::buildFieldParse
- Purpose: Parses module data fields for `StructureBodyModuleData`
- Calls: `ActiveBodyModuleData::buildFieldParse`

### StructureBody::StructureBody
- Purpose: Constructs a `StructureBody` instance
- Calls: Not inferable (constructor body not shown)

### StructureBody::setConstructorObject
- Purpose: Sets the object that built this structure
- Calls: Not inferable

### StructureBody::getConstructorObjectID
- Purpose: Retrieves the ID of the object that built this structure
- Calls: Not inferable

## Globals
- None

## Dependencies
- `ActiveBody.h` (inheritance)
- `MultiIniFieldParse` (used in `buildFieldParse`)
- `ObjectID`, `Thing`, `ModuleData` (forward references)
