# Generals/Code/GameEngine/Source/GameLogic/Object/Body/ImmortalBody.cpp - Enhanced Analysis

## Architectural Role
The `ImmortalBody` class plays a crucial role in the game logic by ensuring that certain objects maintain at least one health point, preventing them from being destroyed. It inherits from `ActiveBody`, extending its functionality to include this immortality trait.

## Cross-References
### Incoming
- Not inferable.

### Outgoing
- Calls into `ActiveBody` for methods like `internalChangeHealth`, `crc`, `xfer`, and `loadPostProcess`.
- Uses functions such as `max`, `getHealth`, and `DEBUG_ASSERTCRASH`.

## Design Patterns
- **Decorator Pattern**: The `ImmortalBody` class extends the functionality of `ActiveBody` by adding behavior to prevent health from dropping below 1, adhering to the decorator pattern.
- **Template Method Pattern**: The methods like `crc`, `xfer`, and `loadPostProcess` follow a template method approach by calling base class methods (`ActiveBody`) and extending their functionality.
