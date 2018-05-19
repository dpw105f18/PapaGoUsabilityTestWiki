defined in header `"idevice.hpp"`

`class IDevice;`

IDevice is an interface which grants use of a GPU on a given computer. It is used for creating all other API objects, which require data to be allocated on the GPU. This Excludes the parser and shaders.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[createSwapChain\|IDevice::createSwapChain]] | Creates a swapchain |
| [[createVertexBuffer\|IDevice::createVertexBuffer]] | Creates a vertex buffer |
| [[createIndexBuffer\|IDevice::createIndexBuffer]] | Creates a index buffer |
| [[createUniformBuffer\|IDevice::createUniformBuffer]] | Creates a uniform buffer |
| [[createDynamicUniformBuffer\|IDevice::createDynamicUniformBuffer]] | Creates a dynamic uniform buffer |
| [[createTextureSamplerD1-3\|IDevice::createTextureSamplerD]] | Creates a 1, 2 or 3 dimensional texture sampler |
| [[createTexture2D\|IDevice::createTexture2D]] | Creates a 2-dimensional texture |
| [[createDepthTexture2D\|IDevice::createDepthTexture2D]] | Creates a 2-dimensional depth texture |
| [[createCommandBuffer\|IDevice::createCommandBuffer]] | Creates a commandbuffer |
| [[createSubCommandBuffer\|IDevice::createSubCommandBuffer]] | Creates a sub-commandbuffer |
| [[createShaderProgram\|IDevice::createShaderProgram]] | Creates a shader program |
| [[createRenderPass\|IDevice::createRenderPass]] | Creates a renderpass |
| [[createGraphicsQueue\|IDevice::createGraphicsQueue]] | Creates a graphicsqueue |
| [[waitIdle\|IDevice::waitIdle]] | Waits until device is idle |
| [[enumerateDevices\|IDevice::enumerateDevices]] |Returns list of avaliable GPU devices on the system |