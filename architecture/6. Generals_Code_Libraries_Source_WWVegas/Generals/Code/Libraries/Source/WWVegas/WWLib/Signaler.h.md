# Generals/Code/Libraries/Source/WWVegas/WWLib/Signaler.h

## Purpose
Template class for establishing bidirectional signal connections between objects.

## Responsibilities
- Manages connections between signaler instances
- Handles signal sending and receiving
- Notifies when connections are dropped
- Prevents copying and assignment

## Key Types
- Signaler<T> (Class): Template class for signal-based communication between objects

## Key Functions
### SignalMe
- Purpose: Connects this signaler to a target signaler
- Calls: Disconnect, Connect

### StopSignaling
- Purpose: Disconnects from a target signaler
- Calls: Disconnect

### SendSignal
- Purpose: Sends a signal to the connected signaler
- Calls: ReceiveSignal (on connected signaler)

### ReceiveSignal
- Purpose: Virtual method for receiving signals (no-op by default)
- Calls: None

### SignalDropped
- Purpose: Called when a connection is dropped
- Calls: None

### Connect
- Purpose: Establishes a connection to a source signaler
- Calls: None

### Disconnect
- Purpose: Breaks the current connection
- Calls: SignalDropped (on connected signaler)

## Globals
- None

## Dependencies
- None (header-only template)
