defined in header `"iimagerresource.hpp"`

`class IImageResource;`

IImageResource is an interface to image data that is located in the GPU. Objects of this class can be used to represent both on and off screen color and depth buffers.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[upload\|IImageResource::upload]] | uploads data to the image |
| [[download\|IImageResource::download]] | downloads the data from the GPU|
| [[inUse\|IImageResource::inUse]] | tells if a buffer is currently being used by the GPU |
| [[getFormat\|IImageResource::getFormat]] | tells the format of the image resource |
