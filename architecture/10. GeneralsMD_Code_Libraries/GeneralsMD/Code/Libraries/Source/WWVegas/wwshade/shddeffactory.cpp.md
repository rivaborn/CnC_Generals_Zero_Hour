# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddeffactory.cpp

## Purpose
Implements the `ShdDefFactoryClass` base class for shader definition factories, handling registration with the manager.

## Responsibilities
- Manages factory registration/unregistration with `ShdDefManagerClass`
- Provides base class for derived shader definition factories
- Maintains linked list pointers (`NextFactory`, `PrevFactory`)

## Key Types
- `ShdDefFactoryClass` (Class): Base class for shader definition factories

## Key Functions
### `ShdDefFactoryClass::ShdDefFactoryClass()`
- Purpose: Constructor that auto-registers the factory with the manager
- Calls: `ShdDefManagerClass::Register_Factory`

### `ShdDefFactoryClass::~ShdDefFactoryClass()`
- Purpose: Destructor that auto-unregisters the factory from the manager
- Calls: `ShdDefManagerClass::Unregister_Factory`

## Globals
- None

## Dependencies
- `shddeffactory.h` (header)
- `shddefmanager.h` (header)
- `ShdDefManagerClass` (external class)
