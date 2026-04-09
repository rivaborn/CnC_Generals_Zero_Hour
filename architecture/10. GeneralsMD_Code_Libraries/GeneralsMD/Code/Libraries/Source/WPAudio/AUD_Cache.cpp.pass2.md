# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Cache.cpp - Enhanced Analysis

## Architectural Role
This file implements the core audio asset caching system for the WPAudio subsystem, bridging between file I/O and audio playback. It manages memory pools, cache eviction policies, and thread-safe access to audio samples, serving as the central resource manager for the game's audio engine.

## Cross-References
### Incoming
- Audio playback systems (e.g., sound event triggers)
- Audio streaming/loading requests from game logic
- Memory management subsystems (for pool allocations)

### Outgoing
- File system (wsys/File.h) for asset loading
- Memory pools (wpaudio/memory.h) for frame/item allocation
- Audio format parsing (AudioFormatReadWaveFile)
- Profiling system (wpaudio/profiler.h) for cache metrics

## Design Patterns
- **Object Pool Pattern**: Uses MemoryPool for AudioCacheItem and AudioFrame to reduce allocation overhead.
- **LRU Cache**: Implements least-recently-used eviction via AudioCacheFreeOldestItem.
- **Resource Locking**: Uses LockAcquire/Release for thread-safe cache item access.

*Not inferable*: Exact relationship with W3D audio mixer or networking audio sync.
