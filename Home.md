# Welcome to the papago-api wiki!
We are building an API on top of Vulkan to rival OpenGL, while still keeping that Vulkan flavor.
The goal of the API is to be a proof of concept, showing that it is possible to build a functional API on top of Vulkan, which can be used for general graphics programming. 

Like Vulkan Papago tries to lower execution time on the GPU. It does this by making render state explicit as objects, so that they can be quickly switched between. In addition, instructions to the GPU are not made through direct function calls, but by building buffers of GPU commands, which are then submitted to the GPU through a queue. This allows commands to be constructed in parallel, but also makes it possible to reuse already constructed command buffers across several frames.

## Status
The API does not include all common graphics API features yet. We have attempted to list these below:
* Usage of the Stencil buffer.
* Configuration of fixed-function pipeline state like rasterizer and output merger state.
* Tesselation, Geometry and Compute shaders are not supported.

## Classes
* [[IDevice|IDevice]]
* [[ISurface|ISurface]]

* Resources
  * [[IBufferResource|IBufferResource]]
  * [[IDynamicBufferResource|IDynamicBufferResource]]
  * [[IImageResource|IImageResource]]
  * [[ISampler|ISampler]]
  * [[ISwapChain|ISwapChain]]

* Command Submission and Execution
  * [[ICommandBuffer|ICommandBuffer]]
  * [[IRecordingCommandBuffer|IRecordingCommandBuffer]]
  * [[ISubommandBuffer|ISubCommandBuffer]]
  * [[IRecordingSubCommandBuffer|IRecordingSubCommandBuffer]]
  * [[IGraphicsQueue|IGraphicsQueue]]
  * [[IRenderPass|IRenderPass]]

* Shader Management
  * [[Parser|Parser]]
  * [[IShader|IShader]]
  * [[IShaderProgram|IShaderProgram]]
* [[API Enums|Enums]] 

## Examples
* [[Single Triangle|Triangle]] (Not yet implemented)
* [[Textured Cubes With Sequential Command Submission| Textured Cubes Sequential]] (Not yet implemented)
* [[Texture Cubes With Parallel Command Submission|Textured Cubes Parallel]] (Not yet implemented)
* [[Shadow Mapping Of Cubes|Shadow Mapping]] (Not yet implemented)


