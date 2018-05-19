defined in header `"icommand_buffer.hpp"`

`class IRecordingCommandBuffer;`

Objects of this class contain GPU commands, which are used to render images to on-screen and off-screen image buffers.
These objects cannot be recorded to directly, but need to be filled with commands through an ICommandBuffer object.

The commands recorded are mainly used to wipe the buffers. 
Actual draw calls are made by ISubCommandBuffers executed on the object.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[execute\|IRecordingCommandBuffer::execute]] | Records the execution of ISubCommandBuffers |
| [[clearColorBuffer\|IRecordingCommandBuffer::clearColorBuffer]] | Records clearing of the color buffer bound to the current render target |
| [[clearDepthStencilBuffer\|IRecordingCommandBuffer::clearDepthStencilBuffer]] | Records the clearing of the combined depth and stencil buffer bound to the current render target.|
| [[clearDepthBuffer\|IRecordingCommandBuffer::clearDepthBuffer]] | Records the clearing of the depth buffer of the bound render target. This buffer must be a depth-only buffer. |
| [[clearStencilBuffer\|IRecordingCommandBuffer::clearStencilBuffer]] | Records the clearing of the stencil buffer of the bound render target. This buffer must be a stencil-only buffer. |
| [[setDynamicIndex\|IRecordingCommandBuffer::setDynamicIndex]] | Records the binding of which index in a IDynamicBuffer to use. |