# GeneralsMD/Code/GameEngine/Include/Common/CustomMatchPreferences.h - Enhanced Analysis

## Architectural Role
This header defines the `CustomMatchPreferences` class, which extends the `UserPreferences` base class to manage game-specific settings for custom matches. It serves as the central data structure for persisting and retrieving user preferences related to multiplayer gameplay, bridging the UI layer with the networking and game logic subsystems.

## Cross-References
### Incoming
- **UI Systems**: Likely called by UI components (e.g., match setup screens) to retrieve/save preferences.
- **Networking Layer**: Used by ladder/online matchmaking systems to restore connection details.
- **Game Initialization**: Accessed during game setup to apply saved preferences (faction, map, etc.).

### Outgoing
- **UserPreferences**: Inherits from this base class, implying it relies on its serialization/deserialization mechanisms.
- **String/Primitive Types**: Uses `AsciiString`, `UnsignedShort`, etc., from the engine's common utilities.

## Design Patterns
- **Property Pattern**: Getter/setter pairs for each preference item, enabling encapsulation and runtime modification.
- **Inheritance**: Extends `UserPreferences`, suggesting a template method or strategy pattern for preference handling.
- **Data Transfer Object (DTO)**: Acts as a container for preference data, decoupling UI/networking from storage logic.

*Not inferable*: No clear use of observer, factory, or other patterns without implementation details.
