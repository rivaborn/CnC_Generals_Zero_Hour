# Generals/Code/Tools/matchbot/wnet/field.h

## Purpose
Defines the `FieldClass` for managing packet field data in network communication.

## Responsibilities
- Encapsulates field data with type, size, and ID
- Provides constructors for different data types
- Supports serialization (Host_To_Net/Net_To_Host)
- Manages memory allocation/deallocation

## Key Types
- **PacketClass (Class)**: Friend class (not defined here)
- **FieldClass (Class)**: Represents a packet field with ID, type, size, and data
- **DataType (Enum)**: Not explicitly defined; values are constants (e.g., `TYPE_CHAR`)

## Key Functions
### FieldClass constructors
- Purpose: Initialize fields for different data types
- Calls: None

### Set methods
- Purpose: Update field data
- Calls: None

### Get_Type
- Purpose: Returns the field's data type
- Calls: None

### Host_To_Net / Net_To_Host
- Purpose: Convert data between host and network byte order
- Calls: None

### Clear
- Purpose: Deallocate memory and zero fields
- Calls: None

## Globals
- **FIELD_HEADER_SIZE (const)**: Size of `FieldClass` minus two pointers
- **TYPE_* (const)**: Data type identifiers (e.g., `TYPE_CHAR`, `TYPE_STRING`)

## Dependencies
- None (standalone header)
