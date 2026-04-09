# Generals/Code/Tools/Babylon/bin.h

## Purpose
Header file defining hash-based container classes for storing and retrieving items by string or integer keys.

## Responsibilities
- Declares `Bin` class for string-keyed storage
- Declares `BinID` class for integer-keyed storage
- Provides hash-based lookup, insertion, and removal operations
- Manages item iteration via `GetNext` methods

## Key Types
- **BinItem (Class)**: Node for string-keyed storage with hash and text fields
- **Bin (Class)**: Hash table using string keys (OLECHAR)
- **BinIDItem (Class)**: Node for integer-keyed storage
- **BinID (Class)**: Hash table using integer keys

## Key Functions
### Bin::calc_hash
- Purpose: Computes hash value for a string key
- Calls: None

### Bin::Add
- Purpose: Inserts an item with string keys into the bin
- Calls: calc_hash

### BinID::Add
- Purpose: Inserts an item with integer key into the bin
- Calls: None

### Bin::Get
- Purpose: Retrieves item by string keys
- Calls: calc_hash, GetBinItem

### BinID::Get
- Purpose: Retrieves item by integer key
- Calls: GetBinIDItem

## Globals
- None

## Dependencies
- `list.h` (ListNode, List)
- `OLEString.h` (OLECHAR)
