# Generals/Code/Tools/Autorun/CDCNTRL.H - Enhanced Analysis

## Architectural Role
This header defines a legacy CD-ROM control utility class used during game installation/autorun, bridging Windows NT and Win9x CD control APIs. It's part of the installation toolchain, not the runtime engine, and reflects early-2000s anti-piracy measures by preventing CD ejection during installation.

## Cross-References
### Incoming
- Likely called by `Generals/Code/Tools/Autorun/` installation executables (e.g., `AUTORUN.CPP`) to enforce CD presence during setup.

### Outgoing
- Directly invokes Windows NT volume management APIs (`Lock_Volume`, `Dismount_Volume`) and Win9x DOS IOCTL calls (`Lock_Logical_Volume`).

## Design Patterns
- **Adapter Pattern**: Abstracts platform-specific CD control APIs (NT vs Win9x) behind a unified interface.
- **Singleton**: Global `CDControl` instance ensures single point of control for CD operations.
- **Platform Abstraction**: Conditional compilation and separate method implementations for Windows variants.
