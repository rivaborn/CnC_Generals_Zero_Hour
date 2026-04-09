# GeneralsMD/Code/GameEngine/Include/GameNetwork/FirewallHelper.h

## Purpose
Header defining the `FirewallHelperClass` for detecting and handling firewall/NAT behaviors in network communication.

## Responsibilities
- Detect firewall/NAT types and behaviors
- Manage spare sockets for testing
- Handle mangler messages for port allocation detection
- Provide firewall behavior queries (NAT, Netgear, etc.)
- Track source port allocation deltas

## Key Types
- **UDP (Class)**: Not inferable (forward declaration).
- **SpareSocketStruct (struct)**: Holds UDP socket and port for spare sockets.
- **FirewallDetectionState (enum)**: States for firewall detection process.
- **ManglerData (struct)**: Data structure for mangler communication (CRC, ports, addresses).
- **ManglerMessage (struct)**: Message wrapper for mangler data.
- **FirewallHelperClass (class)**: Main class for firewall detection and handling.
- **tFirewallBehaviorType (enum)**: Types of firewall behaviors (simple, NAT, port mangling, etc.).

## Key Functions
### createFirewallHelper
- Purpose: Factory function to create `FirewallHelperClass` instance.
- Calls: Not inferable.

### FirewallHelperClass::detectFirewall
- Purpose: Initiate firewall detection process.
- Calls: Not inferable.

### FirewallHelperClass::behaviorDetectionUpdate
- Purpose: Update firewall detection state machine.
- Calls: State-specific update methods (e.g., `detectionTest1Update`).

### FirewallHelperClass::getFirewallBehavior
- Purpose: Retrieve detected firewall behavior type.
- Calls: Not inferable.

### FirewallHelperClass::sendToManglerFromPort
- Purpose: Send data to mangler from a specific source port.
- Calls: Not inferable.

### FirewallHelperClass::getManglerResponse
- Purpose: Retrieve response from mangler for a given packet ID.
- Calls: Not inferable.

## Globals
- **MAX_NUM_MANGLERS (Int)**: Maximum number of manglers (4).
- **MANGLER_PORT (UnsignedShort)**: Port used by manglers (4321).
- **TheFirewallHelper (FirewallHelperClass*)**: Global instance of firewall helper.

## Dependencies
- Key includes: Not inferable (header-only).
- External symbols: `UDP` class (forward-declared), `Bool`, `UnsignedShort`, `Int`, `time_t`.
