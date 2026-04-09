# Generals/Code/Tools/mangler/crc.h

## Purpose
Header file for CRC (Cyclic Redundancy Check) utility functions used in packet validation.

## Responsibilities
- Declares CRC computation and validation functions
- Provides interface for packet integrity checking
- Supports incremental CRC calculation

## Key Types
None

## Key Functions
### Build_Packet_CRC
- Purpose: Computes CRC for a packet buffer including the CRC field
- Calls: Not inferable

### Passes_CRC_Check
- Purpose: Validates packet integrity by checking CRC
- Calls: Not inferable

### Add_CRC
- Purpose: Updates CRC value with additional data
- Calls: Not inferable

## Globals
None

## Dependencies
- Standard C types (unsigned char, unsigned long)
- Boolean type (bool)
