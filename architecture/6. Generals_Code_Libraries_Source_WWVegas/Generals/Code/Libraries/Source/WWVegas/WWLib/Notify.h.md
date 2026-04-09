# Generals/Code/Libraries/Source/WWVegas/WWLib/Notify.h

## Purpose
Implements the Subject-Observer design pattern using C++ templates for event notification.

## Responsibilities
- Defines `Notifier` and `Observer` template classes for event handling
- Provides `TypedEvent`, `TypedEventPtr`, and `TypedEventPair` for event data
- Manages observer registration and notification lifecycle
- Prevents duplicate observer registrations

## Key Types
- `Observer<Event>` (Class): Base class for event observers with notification handling
- `Notifier<Event>` (Class): Manages observer list and event dispatching
- `TypedEvent<Type, Value>` (Class): Wraps event data with subject reference
- `TypedEventPtr<T, Object>` (Class): Pointer-based event wrapper
- `TypedEventPair<A, B>` (Class): Pairs two event data items

## Key Functions
### `Observer::HandleNotification`
- Purpose: Pure virtual method for observers to handle events
- Calls: None

### `Notifier::NotifyObservers`
- Purpose: Notifies all registered observers of an event
- Calls: `Observer::HandleNotification`

### `Notifier::AddObserver`
- Purpose: Registers an observer with the notifier
- Calls: `std::find`, `Observer::NotificationEnded`

### `Notifier::RemoveObserver`
- Purpose: Unregisters an observer from the notifier
- Calls: `std::find`, `Observer::NotificationEnded`

## Globals
- None

## Dependencies
- `<vector>`, `<algorithm>`: STL containers and algorithms
- `assert.h`: Runtime assertions
- `DECLARE_OBSERVER`/`DECLARE_NOTIFIER`: Macros for declaring observer/notifier methods
