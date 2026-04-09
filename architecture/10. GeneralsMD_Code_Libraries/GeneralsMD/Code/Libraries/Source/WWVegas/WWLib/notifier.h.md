# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/notifier.h

## Purpose
Implements the Subject-Observer design pattern using C++ templates for event notification.

## Responsibilities
- Defines `Notifier` and `Observer` template classes for event-driven communication
- Provides typed event wrappers (`TypedEvent`, `TypedEventPtr`, etc.)
- Manages observer registration and notification lifecycle
- Includes utility macros for declaring observers/notifiers

## Key Types
- `Observer<Event>` (Class): Base class for objects that observe events
- `Notifier<Event>` (Class): Base class for objects that notify observers of events
- `TypedEvent<T, V>` (Class): Wraps event data with a unique type
- `TypedEventPtr<T, O>` (Class): Wraps a pointer to an object as an event
- `TypedActionPtr<A, O>` (Class): Extends `TypedEventPtr` with an action value
- `TypedEventPair<A, B>` (Class): Pairs two event items together

## Key Functions
### `Observer::HandleNotification`
- Purpose: Pure virtual method to handle event notifications
- Calls: None

### `Notifier::NotifyObservers`
- Purpose: Notifies all registered observers of an event
- Calls: `Observer::HandleNotification`

### `Notifier::AddObserver`
- Purpose: Registers an observer to receive notifications
- Calls: `std::find`, `Observer::mNotifiers.push_back`

### `Notifier::RemoveObserver`
- Purpose: Unregisters an observer from notifications
- Calls: `std::find`, `Observer::NotificationEnded`

## Globals
- None

## Dependencies
- `<vector>`, `<algorithm>` (STL containers/algorithms)
- `assert.h` (for debugging assertions)
- Uses `std::vector` and `std::find` directly
