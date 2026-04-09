# GeneralsMD/Code/GameEngine/Include/Common/PlayerTemplate.h

## Purpose
Defines player template classes for managing player attributes, resources, and UI elements in the game.

## Responsibilities
- Define `PlayerTemplate` class storing player attributes (name, side, resources, UI elements).
- Provide `PlayerTemplateStore` singleton for managing player templates.
- Parse player template data from INI files.
- Expose accessors for player template properties.

## Key Types
- **PlayerTemplate (Class)**: Stores player attributes (name, side, resources, UI elements).
- **PlayerTemplateStore (Class)**: Singleton managing player templates.
- **PlayerTemplateVector (Class)**: Typedef for `std::vector<PlayerTemplate>`.
- **INI (Class)**: External INI parsing class.
- **FieldParse (Class)**: External field parsing class.
- **Image (Class)**: External image class.

## Key Functions
### `parseStartMoney`
- Purpose: Parse starting money from INI.
- Calls: `INI` methods.

### `parseProductionCostChange`
- Purpose: Parse production cost changes from INI.
- Calls: `INI` methods.

### `parseProductionTimeChange`
- Purpose: Parse production time changes from INI.
- Calls: `INI` methods.

### `parseProductionVeterancyLevel`
- Purpose: Parse production veterancy levels from INI.
- Calls: `INI` methods.

### `parsePlayerTemplateDefinition`
- Purpose: Parse player template definitions from INI.
- Calls: `INI` methods, `PlayerTemplate` constructors.

## Globals
- **ThePlayerTemplateStore (PlayerTemplateStore*)**: Singleton instance of `PlayerTemplateStore`.

## Dependencies
- `Common/SubsystemInterface.h`
- `Common/GameMemory.h`
- `Common/Debug.h`
- `Common/Handicap.h`
- `Common/Money.h`
- `Common/Science.h`
- `Common/AsciiString.h`
- `Common/UnicodeString.h`
- `Common/NameKeyGenerator.h`
- `Common/STLTypedefs.h`
