# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3dtrig.h - Enhanced Analysis

## Architectural Role
This header defines debug trigger IDs for the WW3D rendering subsystem, serving as an interface between the rendering engine and external debug tools. It enables conditional debugging features like render stats display, which are likely toggled via keybindings or console commands.

## Cross-References
### Incoming
- **WWDebug library**: Uses these IDs to check for active debug triggers.
- **Debug UI/Console**: Likely references these constants for trigger activation.

### Outgoing
- None (header-only, no function calls).

## Design Patterns
- **Constant Interface**: Exposes debug trigger IDs as an enum for external systems to reference.
- **Event-Driven Debugging**: Triggers are checked by the WWDebug system, enabling runtime debug feature activation.
- **Not inferable**: No other patterns evident from this header alone.

*[Output under 400 tokens]*
