# GeneralsMD/Code/GameEngine/Include/Common/CopyProtection.h - Enhanced Analysis

## Architectural Role
This header defines the anti-piracy infrastructure for the game, acting as a security layer that integrates with the Windows message pump and launcher process. It's a cross-cutting concern that must be invoked from multiple subsystems (e.g., main loop, initialization, shutdown).

## Cross-References
### Incoming
- Likely called from:
  - Main game loop (for `checkForMessage`)
  - Game initialization (for `validate`)
  - Process shutdown (for `shutdown`)
  - Networking/launcher coordination (for `notifyLauncher`)

### Outgoing
- Interacts with:
  - Windows API (message handling, process checks)
  - Launcher process (IPC via `notifyLauncher`)
  - Memory protection mechanisms (via `s_protectedData`)

## Design Patterns
- **Singleton-like behavior**: Static-only class with no instance methods, suggesting global access pattern
- **Facade pattern**: Hides complex copy protection logic behind simple interface
- **Feature flag pattern**: Uses `DO_COPY_PROTECTION` macro to conditionally compile protection code

*Not inferable*: Exact IPC mechanism with launcher, memory protection implementation details.
