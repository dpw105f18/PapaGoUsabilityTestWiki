defined in header `"ibufferresource.hpp"`

`class IDynamicBufferResource;`

IDynamicBufferResource is an interface to a dynamic buffer in the GPU.
Different from an IBufferResource, this class may contain several sub resources, which can be switched between using commands. 

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[upload\|IDynamicBufferResource::upload]] | uploads data to the buffer |
| [[download\|IDynamicBufferResource::download]] | download the data from the buffer |
| [[inUse\|IDynamicBufferResource::inuse]] | tells if a buffer is currently being used by the GPU |