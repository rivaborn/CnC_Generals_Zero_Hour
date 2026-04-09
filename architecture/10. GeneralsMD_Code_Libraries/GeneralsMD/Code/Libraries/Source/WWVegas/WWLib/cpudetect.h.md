# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/cpudetect.h

## Purpose
Header file for CPU detection and feature identification in the SAGE engine.

## Responsibilities
- Define CPU detection class and related types
- Provide accessors for CPU features, cache info, and memory stats
- Declare CPUID instruction handling
- Expose processor manufacturer and model identification

## Key Types
- **CPUDetectClass (Class)**: Main CPU detection interface
- **ProcessorManufacturerType (Enum)**: CPU manufacturer identifiers
- **IntelProcessorType (Enum)**: Intel processor model identifiers
- **AMDProcessorType (Enum)**: AMD processor model identifiers
- **VIAProcessorType (Enum)**: VIA processor model identifiers
- **RiseProcessorType (Enum)**: Rise processor model identifiers
- **CPUIDStruct (Struct)**: Wrapper for CPUID instruction results

## Key Functions
### CPUID
- Purpose: Execute CPUID instruction with given type
- Calls: None (direct hardware instruction)

### Get_Processor_Manufacturer_Name
- Purpose: Return human-readable manufacturer name
- Calls: None

### Get_Feature_Bits / Get_Extended_Feature_Bits
- Purpose: Return CPUID feature flags
- Calls: None

## Globals
- **ProcessorLog (StringClass)**: Detailed CPU detection log
- **CompactLog (StringClass)**: Compact CPU detection summary
- **ProcessorType/ProcessorFamily/ProcessorModel/ProcessorRevision (int)**: CPU identification values
- **ProcessorSpeed/ProcessorTicksPerSecond/InvProcessorTicksPerSecond (int/sint64/double)**: CPU speed metrics
- **FeatureBits/ExtendedFeatureBits (unsigned)**: CPUID feature flags
- **L2CacheSize/L2CacheLineSize/L2CacheSetAssociative (unsigned)**: L2 cache parameters
- **L1DataCacheSize/L1DataCacheLineSize/L1DataCacheSetAssociative (unsigned)**: L1 data cache parameters
- **L1InstructionCacheSize/L1InstructionCacheLineSize/L1InstructionCacheSetAssociative (unsigned)**: L1 instruction cache parameters
- **L1InstructionTraceCacheSize/L1InstructionTraceCacheSetAssociative (unsigned)**: L1 trace cache parameters
- **TotalPhysicalMemory/AvailablePhysicalMemory/TotalPageMemory/AvailablePageMemory/TotalVirtualMemory/AvailableVirtualMemory (unsigned)**: System memory stats
- **HasCPUIDInstruction/HasRDTSCInstruction/HasSSESupport/HasSSE2Support/HasCMOVSupport/HasMMXSupport/Has3DNowSupport/HasExtended3DNowSupport (bool)**: Feature detection flags
- **VendorID (char[20])/ProcessorString (char[48])**: CPU identification strings

## Dependencies
- "always
