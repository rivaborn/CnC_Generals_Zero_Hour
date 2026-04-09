# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_List.cpp - Enhanced Analysis

## Architectural Role
This file implements a generic doubly-linked list with priority-based sorting, serving as a foundational data structure for the WPAudio subsystem. It's likely used for managing audio resource queues, playback priorities, or event scheduling within the audio engine.

## Cross-References
### Incoming
- Audio playback management (e.g., sound queueing)
- Resource loading/unloading systems
- Event-driven audio triggers

### Outgoing
- Core memory allocation (via `new`/`delete`)
- WPAudio-specific types (`ListHead`, `ListNode`)

## Design Patterns
- **Composite Pattern**: List nodes can contain other nodes, forming a tree-like structure.
- **Priority Queue**: `ListAddNodeSortAscending` enforces ordered insertion based on priority.
- **Iterator Pattern**: `ListNodeNext`/`ListNodePrev` provide traversal without exposing internal structure.

*Not inferable*: Exact usage in audio subsystem (e.g., voice allocation, streaming buffers).
