defined in header `"ibufferresource.hpp"`

`class IBufferResource;`

IBufferResource is an interface to a buffer of data on the GPU.
This class is used to create both index and vertex buffers, but also static uniform buffers, which are bound to shaders. 

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[upload\|IBufferResource::upload]] | uploads data to the buffer |
| [[download\|IBufferResource::download]] | download the data from the buffer |
| [[inUse\|IBufferResource::inuse]] | tells if a buffer is currently being used by the GPU |

## Example
```C++
#include <vector>
#include <windows.h>
#include "idevice.hpp"
#include "ibufferrsource.hpp"
#include "isurface.hpp"

#define HEIGHT = 600;
#define WIDTH = 800;

struct V { float x, y, z; }

const std::vector<V> v {
  {-0.5, -0.5, 0.0},
  {-0.5,  0.5, 0.0},
  { 0.5,  0.5, 0.0},
  { 0.5, -0.5, 0.0}
};

const std::vector<unsigned int> i {
   0, 1, 2,
   0, 2, 3
};

int main() {
    /*
  setup code omitted
  */

  auto vb = device->createVertexBuffer(v); // vb points to a vertex buffer
  auto ib = device->createIndexBuffer(i); // ib points to an index buffer
  auto ub = device->createUniformBuffer(64); // ub points to an uniform buffer with 64 bytes of storage
}
```