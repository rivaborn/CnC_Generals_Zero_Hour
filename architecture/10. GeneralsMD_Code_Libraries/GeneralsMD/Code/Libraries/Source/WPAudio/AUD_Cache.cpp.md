# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Cache.cpp

## Purpose
Manages audio asset caching for the game's audio system, handling loading, storage, and retrieval of audio samples.

## Responsibilities
- Creates and destroys audio cache instances
- Loads and caches audio assets from files
- Manages cache eviction when full
- Provides thread-safe access to cached items
- Tracks cache performance metrics

## Key Types
- AudioCache (struct): Main cache container managing frames and items
- AudioCacheItem (struct): Represents a cached audio asset with its frames
- AudioFrame (struct): Contains audio data for a portion of a sample

## Key Functions
### AudioCacheCreate
- Purpose: Initializes a new audio cache with specified size and item limits
- Calls: MemoryPoolCreate, ListInit, AudioFormatInit, ProfCacheInit

### AudioCacheLoadItem
- Purpose: Loads an audio asset into cache or retrieves it if already cached
- Calls: AudioCacheGetItem, audioCacheAssetOpen, MemoryPoolGetItem, AudioCacheFreeOldestItem, AudioSampleAddFrame, audioCacheAssetRead

### AudioCacheFreeOldestItem
- Purpose: Removes the oldest unused item from cache to make space
- Calls: AudioCacheItemInUse, AudioCacheItemFree

### AudioCacheItemFree
- Purpose: Releases all resources associated with a cache item
- Calls: ListNodeRemove, AudioFrameDeinit, MemoryPoolReturnItem, AudioSampleDeinit

## Globals
- AudioCache (struct): Main cache container
- AudioCacheItem (struct): Cached audio asset representation
- audioCacheAssetClose (function): Closes current asset file
- audioCacheAssetOpen (function): Opens specified audio asset
- audioCacheAssetRead (function): Reads data from current asset file

## Dependencies
- wpaudio/altypes.h, wpaudio/memory.h, wpaudio/list.h, wpaudio/source.h, wpaudio/cache.h, wpaudio/profiler.h
- wsys/File.h
- MemoryPoolCreate/Destroy, ListInit/Append/Remove, AudioFormatInit/ReadWaveFile, ProfCacheInit/Hit/Miss/LoadStart/End/AddLoadBytes/AddPage/Fill/Remove/RemovePage/UpdateInterval
- LockAcquire/Release/Locked, AudioSampleInit/Deinit/AddFrame/SetName, AudioFrameInit/Deinit
