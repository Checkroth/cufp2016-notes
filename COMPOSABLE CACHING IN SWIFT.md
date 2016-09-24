# Introduction
- Brandon Kase
- Pinterest
- SWIFT
- Slides https://is.gd/edLKW7

# Caching
- Key comes in
- Check ram
- Check disk
- Check network
- Write to disk/ram if needed
- Error if not found anywhere

# In Swift
##Cache protocol
- Associated types
- Get methods
	- `Key -> F[V]`
- Set methods
	-`[key, value] -> F[R]`
- Back cache with key hashmap
- Binding with type alias (in swift)
## Cache Layering
- Key and Value same for all caches
- Link multiple caches together to propogate key/value
- Combine in to _one cache_
- Model network as cache
- Compositions are associative 
	- `((c1 comp c2) comp c3) $eq (c1 comp (c2 comp c3))`
- Caches are *monoids*
	- Speaker says associative + identity = monoid
	- Zero value?
## Transforming Things
- Compose multiple cache in to one cache
- returning bit maps
- Key transformation
	- Can get / set from new cache to old cache
- Results in uniform cache that takes all keys
	- figures out right place for right k

## Optimize
- Utilize dictionary
- Creates map from key/v searches
- Can be applied to any cache (abstracted)

# Specifics
- Carlos Caching
	- Open source swift library for caching
- Purescript implementation


- Q write to both asynchronously -- need key/v to be same across caches