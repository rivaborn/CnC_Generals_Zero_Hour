# GeneralsMD/Code/GameEngine/Source/Common/System/CriticalSection.cpp

## Purpose
Defines global critical section objects used for thread synchronization across the game engine.

## Responsibilities
- Declares global critical section instances for string, DMA, memory pool, and debug log operations.
- Initializes a performance gathering object for critical section timing (when PERF_TIMERS is enabled).

## Key Types
None

## Key Functions
None

## Globals
- TheAsciiStringCriticalSection (FastCriticalSectionClass): Thread synchronization for ASCII string operations.
- TheUnicodeStringCriticalSection (CriticalSection*): Thread synchronization for Unicode string operations.
- TheDmaCriticalSection (CriticalSection*): Thread synchronization for DMA operations.
- TheMemoryPoolCriticalSection (CriticalSection*): Thread synchronization for memory pool operations.
- TheDebugLogCriticalSection (CriticalSection*): Thread synchronization for debug logging.
- TheCritSecPerfGather (PerfGather): Performance timer for critical section operations (conditional).

## Dependencies
- "PreRTS.h": Required header for all GameEngine C++ files.
- "Common/CriticalSection.h": Header defining CriticalSection and FastCriticalSectionClass.
- PERF_TIMERS: Conditional compilation for performance timing.
