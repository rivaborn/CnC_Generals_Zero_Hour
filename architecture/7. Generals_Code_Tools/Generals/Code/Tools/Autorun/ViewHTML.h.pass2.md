# Generals/Code/Tools/Autorun/ViewHTML.h - Enhanced Analysis

## Architectural Role
This header defines the interface for launching external web content from the game's autorun tool, bridging the game's tooling layer with the host system's default browser. It supports asynchronous execution via callbacks, likely used for post-installation documentation or updates.

## Cross-References
### Incoming
- `Generals/Code/Tools/Autorun/*.cpp`: Autorun tool components that need to display web-based content (e.g., EULA, help pages).
- `Generals/Code/Tools/Setup/*.cpp`: Installer/updater logic requiring external browser access.

### Outgoing
- **OS Abstraction Layer**: Calls into platform-specific browser launch APIs (not inferable from header).
- `CallbackHook.h`: Uses the callback mechanism for async notification.

## Design Patterns
- **Facade Pattern**: Abstracts browser launch complexity behind a simple function.
- **Observer Pattern**: Callback parameter enables decoupled notification of completion.
- **Dependency Injection**: Callback is injected at call-site, allowing flexible behavior.

*Not inferable*: No other patterns evident from header alone.
