# GeneralsMD/Code/GameEngine/Include/Common/CriticalSection.h

## Purpose
Provides thread synchronization utilities using Windows critical sections and a scoped RAII wrapper.

## Responsibilities
- Wraps Windows CRITICAL_SECTION for thread-safe code blocks
- Offers scoped locking via RAII pattern
- Manages global critical sections for string/DMA/memory/debug operations
- Supports performance timing for critical section operations

## Key Types
- **CriticalSection (Class)**: Wrapper for Windows critical section with enter/exit methods
- **ScopedCriticalSection (Class)**: RAII wrapper that auto-locks/unlocks a CriticalSection
- **FastCriticalSectionClass (Class)**: Not defined here (included from mutex.h)

## Key Functions
### CriticalSection::enter
- Purpose: Acquires the critical section lock
- Calls: `EnterCriticalSection`, `AutoPerfGather` (if PERF_TIMERS enabled)

### CriticalSection::exit
- Purpose: Releases the critical section lock
- Calls: `LeaveCriticalSection`, `AutoPerfGather` (if PERF_TIMERS enabled)

### ScopedCriticalSection::ScopedCriticalSection
- Purpose: Locks the associated CriticalSection in constructor
- Calls: `CriticalSection::enter`

### ScopedCriticalSection::~ScopedCriticalSection
- Purpose: Unlocks the associated CriticalSection in destructor
- Calls: `CriticalSection::exit`

## Globals
- **TheAsciiStringCriticalSection (FastCriticalSectionClass)**: Global lock for ASCII string operations
- **TheUnicodeStringCriticalSection (CriticalSection*)**: Global lock for Unicode string operations
- **TheDmaCriticalSection (CriticalSection*)**: Global lock for DMA operations
- **TheMemoryPoolCriticalSection (CriticalSection*)**: Global lock for memory pool operations
- **TheDebugLogCriticalSection (CriticalSection*)**:
