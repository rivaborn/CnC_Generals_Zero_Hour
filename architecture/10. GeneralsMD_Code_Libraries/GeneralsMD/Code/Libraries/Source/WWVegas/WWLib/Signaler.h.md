# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Signaler.h

## Purpose
Lightweight two-way notification system enabling loose coupling between two classes.

## Responsibilities
- Manages bidirectional signal connections between instances
- Handles signal sending and receiving
- Tracks connection state and notifies when connections drop
- Prevents copying/assignment to maintain single ownership

## Key Types
- **Signaler<T> (Class)**: Template class for two-way signal communication between objects.

## Key Functions
### SignalMe
- Purpose: Establishes bidirectional connection with another Signaler.
- Calls: Disconnect(), Connect()

### StopSignaling
- Purpose: Terminates connection with a specific Signaler.
- Calls: Disconnect()

### SendSignal
- Purpose: Sends a signal to the connected Signaler.
- Calls: ReceiveSignal() (on target)

### ReceiveSignal
- Purpose: Virtual hook for receiving signals (no-op by default).
- Calls: None

### SignalDropped
- Purpose: Notification when connection is lost.
- Calls: None

### Connect
- Purpose: Internal method to establish connection.
- Calls: None

### Disconnect
- Purpose: Internal method to break connection.
- Calls: SignalDropped() (on target)

## Globals
- None

## Dependencies
- None (header-only template implementation)
