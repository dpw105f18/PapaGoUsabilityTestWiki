defined in header `"isampler.hpp"`

`class ISampler;`

ISampler is an interface class for Samplers, it does not come with any functions but is used internally in Papago API when creating Samplers for render passes when recording commands. These samplers can be 1, 2 or 3 dimensional.

Please see [IDevice-createTextureSamplerD1-3](https://github.com/dpw105f18/papago-api/wiki/IDevice%3A%3AcreateTextureSamplerD) documentation for code examples on how to create samplers.