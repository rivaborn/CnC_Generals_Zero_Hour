# Generals/Code/Tools/Babylon/bin.cpp

## Purpose
Implements hash-based container classes for storing and retrieving items by string keys or integer IDs.

## Responsibilities
- Provides `Bin` class for string-keyed storage/retrieval
- Provides `BinID` class for integer-ID storage/retrieval
- Manages item addition, removal, and lookup
- Handles memory cleanup for stored items

## Key Types
- `Bin` (Class): String-keyed hash container
- `BinItem` (Class): Item stored in `Bin` with string keys
- `BinID` (Class): Integer-ID hash container
- `BinIDItem` (Class): Item stored in `BinID` with integer ID

## Key Functions
### `Bin::Get`
- Purpose: Retrieves item by string keys
- Calls: `GetBinItem`

### `Bin::Add`
- Purpose: Adds item with string keys to container
- Calls: `calc_hash`, `new BinItem`

### `Bin::GetBinItem`
- Purpose: Finds item matching string keys
- Calls: `calc_hash`, `GetNextBinItem`

### `BinID::Get`
- Purpose: Retrieves item by integer ID
- Calls: `GetBinIDItem`

### `BinID::Add`
- Purpose: Adds item with integer ID to container
- Calls: `new BinIDItem`

## Globals
- None

## Dependencies
- `stdAfx.h`, `bin.h`, `assert.h`, `list.h`
- Uses `List` class for bucket storage
- Uses `OLECHAR` for string keys
