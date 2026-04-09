# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HackInternetAIUpdate.h - Enhanced Analysis

## Architectural Role
This file implements the AI logic for the "Hack Internet" ability, a unique unit behavior in Generals/Zero Hour. It extends the AI update system with a state machine pattern to manage the hacking sequence (unpacking, hacking, packing) and cash generation mechanics.

## Cross-References
### Incoming
- AI system calls `update()` to process hacking state transitions
- Unit command system invokes `aiDoCommand()` for hacking orders
- Game logic queries `isHacking()`/`isHackingPackingOrUnpacking()` for state checks

### Outgoing
- Uses `StateMachine` base class for state management
- Leverages `AIUpdateModuleData` for configuration parsing
- Interacts with `Xfer` for serialization (network/savegame support)

## Design Patterns
- **State Pattern**: Encapsulates hacking behavior in discrete states (Unpacking/Hacking/Packing)
- **Module Pattern**: Follows SAGE's AI module architecture for configuration and behavior separation
- **Strategy Pattern**: `HackInternetAIInterface` provides a pluggable interface for hacking state queries

*Not inferable*: Exact command processing flow in `aiDoCommand()` or cash generation logic in `update()`.
