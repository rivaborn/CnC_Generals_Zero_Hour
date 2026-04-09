# Generals/Code/GameEngine/Source/Common/Thing/ThingFactory.cpp

## Purpose
This file implements the `ThingFactory` class, responsible for managing and creating game objects (things) using templates.

## Responsibilities
- Manages a database of thing templates.
- Creates new things based on templates.
- Handles overrides and reskinning of templates.
- Parses object definitions from INI files.
- Ensures unique template names and IDs.

## Key Types
- `ThingFactory` (Class): Manages the creation and management of game objects using templates.
- `TEMPLATE_HASH_SIZE` (Enum): Defines the size of the hash map for storing templates.

## Key Functions
### freeDatabase
- Purpose: Frees all data loaded into the template database.
- Calls: `deleteInstance`, `clear`

### addTemplate
- Purpose: Adds a new thing template to the database.
- Calls: `find`, `friend_setNextTemplate`

### ThingFactory Constructor
- Purpose: Initializes the `ThingFactory` instance.
- Calls: `resize`

### ThingFactory Destructor
- Purpose: Frees all template data on destruction.
- Calls: `freeDatabase`

### newTemplate
- Purpose: Creates a new template with a unique identifier and adds it to the list.
- Calls: `newInstance`, `findTemplate`, `friend_setTemplateID`, `friend_setTemplateName`, `addTemplate`

### newOverride
- Purpose: Creates an override for an existing template.
- Calls: `newInstance`, `friend_getFinalOverride`, `markAsOverride`, `setNextOverride`

### init
- Purpose: Initializes the factory (currently empty).

### reset
- Purpose: Resets the factory by deleting overrides and removing templates created for the current map.
- Calls: `deleteOverrides`, `erase`

### update
- Purpose: Updates the factory (currently empty).

### findByTemplateID
- Purpose: Returns a template by its ID.
- Calls: `getTemplateID`

### findTemplateInternal
- Purpose: Finds a template by name, optionally loading it if not found.
- Calls: `find`, `initForLTA`

### newObject
- Purpose: Creates a new game object based on a template.
- Calls: `friend_createObject`, `onCreate`, `registerObject`, `initObject`

### newDrawable
- Purpose: Creates a new drawable object based on a template.
- Calls: `friend_createDrawable`

### parseObjectDefinition
- Purpose: Parses an object definition from an INI file and updates the corresponding template.
- Calls: `findTemplateInternal`, `newTemplate`, `newOverride`, `copyFrom`, `initFromINI`, `validate`

## Globals
- `TheThingFactory` (ThingFactory*): Singleton instance of the thing factory.

## Dependencies
- Key includes:
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/FileSystem.h"
  - "Common/GameAudio.h"
  - "Common/MapObject.h"
  - "Common/ModuleFactory.h"
  - "Common/RandomValue.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/CreateModule.h"
  - "Common/ProductionPrerequisite.h"
  - "GameClient/GameClient.h"
  - "GameClient/Drawable.h"
  - "Common/INI.h"
