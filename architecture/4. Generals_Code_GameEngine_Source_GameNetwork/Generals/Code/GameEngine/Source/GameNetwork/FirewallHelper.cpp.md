# Generals/Code/GameEngine/Source/GameNetwork/FirewallHelper.cpp

## Purpose
Handles firewall detection and NAT traversal for network connectivity in Command & Conquer Generals.

## Responsibilities
- Detects firewall behavior types (simple, mangling, port allocation schemes)
- Manages temporary UDP sockets for firewall testing
- Calculates firewall "hardness" and retry estimates
- Communicates with mangler servers to test firewall behavior

## Key Types
- FirewallHelperClass: Main class handling firewall detection logic
- FirewallBehaviorType (enum): Represents different firewall behaviors (simple, mangling, port allocation)
- ManglerMessage: Packet structure for communicating with mangler servers

## Key Functions
### createFirewallHelper
- Purpose: Factory function to create FirewallHelperClass instance
- Calls: None

### detectFirewall
- Purpose: Initiates firewall detection if behavior is unknown
- Calls: detectFirewallBehavior, behaviorDetectionUpdate

### getNextTemporarySourcePort
- Purpose: Allocates temporary UDP ports for firewall testing
- Calls: openSpareSocket, closeSpareSocket

### sendToManglerFromPort
- Purpose: Sends test packets to mangler servers from specific ports
- Calls: byteAdjust, CRC::computeCRC, UDP::Write

### getNATPortAllocationScheme
- Purpose: Analyzes port allocation patterns from NAT devices
- Calls: None

## Globals
- TheFirewallHelper (FirewallHelperClass*): Singleton instance of firewall helper

## Dependencies
- Common/crc.h, Common/UserPreferences.h
- GameNetwork/NAT.h, GameNetwork/udp.h, GameNetwork/NetworkDefs.h
- GameNetwork/GameSpy/GSConfig.h
- PreRTS.h (must be first include)
