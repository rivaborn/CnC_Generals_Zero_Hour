# GeneralsMD/Code/GameEngine/Source/GameNetwork/FirewallHelper.cpp

## Purpose
Handles firewall detection and NAT traversal for network connectivity in Command & Conquer Generals.

## Responsibilities
- Detects firewall behavior types (simple, mangling, port allocation schemes)
- Manages temporary UDP sockets for firewall testing
- Calculates firewall "hardness" and retry estimates
- Communicates with mangler servers to test firewall behavior

## Key Types
- FirewallHelperClass: Main firewall detection and management class
- FirewallBehaviorType (enum): Represents different firewall behaviors (simple, mangling, port allocation)
- SpareSocketStruct: Tracks temporary UDP sockets used for testing

## Key Functions
### createFirewallHelper
- Purpose: Factory function to create FirewallHelperClass instance
- Calls: None

### detectFirewall
- Purpose: Initiates firewall detection if behavior is unknown
- Calls: detectFirewallBehavior, behaviorDetectionUpdate

### getNATPortAllocationScheme
- Purpose: Analyzes port allocation patterns from NAT devices
- Calls: None

### getFirewallHardness
- Purpose: Calculates a numeric value representing firewall difficulty
- Calls: None

### openSpareSocket/closeSpareSocket
- Purpose: Manages temporary UDP sockets for firewall testing
- Calls: UDP::Bind

## Globals
- TheFirewallHelper (FirewallHelperClass*): Singleton instance of firewall helper
- FirewallHelperClass::m_sourcePortPool (Int): Base port number for temporary sockets

## Dependencies
- Common/crc.h, Common/UserPreferences.h
- GameNetwork/NAT.h, GameNetwork/udp.h, GameNetwork/NetworkDefs.h
- GameNetwork/GameSpy/GSConfig.h
- Uses UDP networking, CRC computation, and preference system
