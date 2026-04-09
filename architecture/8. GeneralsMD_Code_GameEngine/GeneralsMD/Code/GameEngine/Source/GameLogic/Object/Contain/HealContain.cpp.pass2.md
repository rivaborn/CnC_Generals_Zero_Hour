# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/HealContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the healing container system, a specialized variant of the `OpenContain` module. It handles gradual health restoration for contained objects over time, integrating with the game's damage/healing system and object containment framework.

## Cross-References
### Incoming
- **GameLogic/Module/HealContain.h**: Defines the class interface
- **GameLogic/Object/Contain/OpenContain.cpp**: Base class implementation
- **GameLogic/Module/BodyModule.h**: For health management
- **GameLogic/Damage.h**: For healing damage types

### Outgoing
- **GameLogic/Module/OpenContain.h**: Base class methods
- **GameLogic/Module/BodyModule.h**: Health queries and healing
- **GameLogic/GameLogic.h**: Frame counter access
- **Common/Xfer.h**: Serialization support

## Design Patterns
- **Template Method**: Extends `OpenContain` with healing-specific behavior while preserving base functionality
- **Strategy**: Healing logic is encapsulated in `doHeal`, allowing for different healing strategies
- **Observer**: Objects are notified of healing via the damage system (implicit pattern)

*Not inferable*: No clear use of Factory, Decorator, or Visitor patterns in this file.
