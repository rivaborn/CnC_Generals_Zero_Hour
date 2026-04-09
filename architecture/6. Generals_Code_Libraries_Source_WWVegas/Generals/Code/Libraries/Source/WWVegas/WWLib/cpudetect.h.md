# Generals/Code/Libraries/Source/WWVegas/WWLib/cpudetect.h

## Purpose
Header file for CPU detection and feature querying in the SAGE engine.

## Responsibilities
- Define CPU detection class and related types
- Provide accessors for CPU features, cache info, and memory
- Declare CPUID instruction wrapper
- Expose processor manufacturer and model enums

## Key Types
- **CPUDetectClass (Class)**: Main CPU detection interface
- **ProcessorManufacturerType (Enum)**: CPU vendor identifiers (Intel, AMD, etc.)
- **IntelProcessorType (Enum)**: Intel processor model identifiers
- **AMDProcessorType (Enum)**: AMD processor model identifiers
- **VIAProcessorType (Enum)**: VIA processor model identifiers
- **RiseProcessorType (Enum)**: Rise processor model identifiers
- **CPUIDStruct (Struct)**: CPUID result container

## Key Functions
### CPUID
- Purpose: Execute CPUID instruction with given type
- Calls: None (direct hardware instruction)

### Get_Processor_Manufacturer
- Purpose: Return detected CPU manufacturer
- Calls: None

### Get_Processor_Speed
- Purpose: Return detected CPU clock speed
- Calls: None

### Get_Feature_Bits
- Purpose: Return CPUID feature flags
- Calls: None

## Globals
- **ProcessorLog (StringClass)**: Detailed CPU detection log
- **CompactLog (StringClass)**: Compact CPU detection log
- **ProcessorManufacturer (ProcessorManufacturerType)**: Detected CPU vendor
- **FeatureBits (unsigned)**: CPUID feature flags
- **L2CacheSize (unsigned)**: Detected L2 cache size

## Dependencies
- "always.h" - Common header
- "wwstring.h" - String class
- Platform-specific sint64 typedef (WIN32/_UNIX)
