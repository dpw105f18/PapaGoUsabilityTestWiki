defined in header `"iswapchain.hpp"`

`class ISwapchain;`

Interface for the SwapChain class. A swapchain contains 1 or more on-screen framebuffers. Right now it can only be used for triple buffering. When an image from a swapchain is presented the front and back buffers are automatically switched around.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[getWidth\|ISwapchain::getWidth]] | Returns the width of the swapchain |
| [[getHeight\|ISwapchain::getHeight]] | Returns the height of the swapchain |
| [[getFormat\|ISwapchain::getFormat]] | Returns the format of the swapchain |

## Enums
| PresentMode  |
| ------------- |
| eMailbox |

## Example
```c++
#include "isurface.hpp"
#include "idevice.hpp"
#include "api_enums.hpp"
#include "iswapchain.hpp"

int main()
{
   /*
   setup code omitted
   */ 
   
   //Get the path to the GLSL-SPIRV compiler
   auto parser = Parser("[Filepath to VulkanSDK]/VulkanSDK/1.0.65.0/Bin32/glslangValidator.exe");

   //Compilation of shaders
   auto vertexShader = parser.compileVertexShader(readFile("shader/vertexShader.vert"), "main");
   auto fragmentShader = parser.compileVertexShader(readFile("shader/fragmentShader.frag"), "main");

   //Creation of shader program
   auto shaderProgram = device->createShaderProgram(*vertexShader, *fragmentShader);

   //Create a SwapChain
   auto swapChain = device->createSwapChain(Format::eR8G8B8A8Unorm, Format::eD32Sfloat, 3, IDevice::PresentMode::eMailbox);

   //Creation of RenderPass: This is where the getters from ISwapChain become useful.
   auto renderPass = device->createRenderPass(*shaderProgram, swpaChain->getWidth(), swapChain->getHeight(), swapChain->getFormat(), Format::eD32Sfloat);
}