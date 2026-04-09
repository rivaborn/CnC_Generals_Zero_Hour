# GeneralsMD/Code/GameEngine/Include/GameNetwork/WOLBrowser/WebBrowser.h - Enhanced Analysis

## Architectural Role
This file defines the COM-based embedded browser subsystem, bridging the game engine with Windows' WebBrowser control (via EABrowserDispatch). It's part of the WOL (Westwood Online) networking layer, enabling in-game web content display (e.g., EA's Dune Emperor browser feature).

## Cross-References
### Incoming
- Likely called by UI/front-end systems (e.g., menu screens) needing embedded browser functionality
- May be referenced by WOL networking code for online content integration

### Outgoing
- Uses `FEBDispatch` for COM interface implementation
- Depends on `GameWindow` for window management (rendering subsystem)
- Interacts with `EABrowserDispatch` for low-level browser control

## Design Patterns
- **COM Interface Pattern**: Uses `FEBDispatch` to implement `IBrowserDispatch`, enabling cross-process communication with the browser control
- **Singleton Pattern**: `TheWebBrowser` provides global access to the browser subsystem
- **Memory Pool Pattern**: `WebBrowserURL` uses `MemoryPoolObject` for optimized allocation/deallocation

*Not inferable*: Exact usage of `WebBrowserURL` linked list or `QueryInterface` implementation details.
