# Generals/Code/Tools/mangler/wnet/field.h

## Purpose
Defines the `FieldClass` for managing packet fields in network communication.

## Responsibilities
- Encapsulates field data with type, size, and ID
- Provides constructors for different data types
- Supports serialization (Host_To_Net/Net_To_Host)
- Manages field list for packet processing

## Key Types
- **FieldClass (Class)**: Represents a packet field with ID, type, size, and data
- **PacketClass (Class)**: Friend class (not defined here)

## Key Functions
### FieldClass constructors
- Purpose: Initialize fields for different data types
- Calls: None

### Set methods
- Purpose: Update field data
- Calls: None

### Get_Type
- Purpose: Returns the data type of the field
- Calls: None

### Get_Data
- Purpose: Returns the field's data pointer
- Calls: None

### Host_To_Net / Net_To_Host
- Purpose: Convert between host and network byte order
- Calls: None

## Globals
- **TYPE_CHAR (const)**: 1 (char type ID)
- **TYPE_UNSIGNED_CHAR (const)**: 2 (unsigned char type ID)
- **TYPE_SHORT (const)**: 3 (short type ID)
- **TYPE_UNSIGNED_SHORT (const)**: 4 (unsigned short type ID)
- **TYPE_LONG (const)**: 5 (long type ID)
- **TYPE_UNSIGNED_LONG (const)**: 6 (unsigned long type ID)
- **TYPE_STRING (const)**: 7 (string type ID)
- **TYPE_CHUNK (const)**: 20 (chunk type ID)
- **FIELD_HEADER_SIZE (const)**: Size of FieldClass minus two pointers

## Dependencies
- None (header-only, no
