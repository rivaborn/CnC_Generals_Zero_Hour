# GeneralsMD/Code/GameEngine/Include/Common/ThingTemplate.h

## Purpose
Defines the `ThingTemplate` class and related types for game entity definitions in Command & Conquer Generals.

## Responsibilities
- Declares the `ThingTemplate` class for entity blueprints
- Defines audio, build, and module-related enums
- Provides parsing infrastructure for game data
- Manages module information and inheritance

## Key Types
- **ThingTemplate (Class)**: Core template for game entities (units, buildings, etc.)
- **ThingTemplateAudioType (Enum)**: Audio event types for entities
- **BuildCompletionType (Enum)**: How entities appear when built
- **BuildableStatus (Enum)**: Buildability flags
- **ModuleInfo (Class)**: Container for module data and inheritance
- **AudioArray (Class)**: Manages audio events for templates

## Key Functions
### parsePrerequisites
- Purpose: Parses prerequisite data from INI files
- Calls: Not inferable

### parseModuleName
- Purpose: Parses module names during template loading
- Calls: Not inferable

### getBuildFacilityTemplate
- Purpose: Returns the build facility template for this entity
- Calls: Not inferable

### validate
- Purpose: Validates template data integrity
- Calls: Not inferable

## Globals
- **s_objectFieldParseTable (FieldParse[])**: Parse table for object fields
- **s_objectReskinFieldParseTable (FieldParse[])**: Parse table for reskin fields
- **s_audioEventNoSound (AudioEventRTS)**: Default silent audio event

## Dependencies
- `AudioEventRTS`, `GeometryInfo`, `KindOf`, `ModuleFactory`, `Overridable`
- `WeaponSet`, `ArmorSet`, `ProductionPrerequisite`, `Science`
- `Image`, `Player`, `INI` (forward declarations)
