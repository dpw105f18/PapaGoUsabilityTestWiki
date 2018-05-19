defined in header `"icommand_buffer.hpp"`

`class IRecordingSubCommandbuffer;`

Objects of this class contain GPU commands, which are used to render images to on-screen and off-screen image buffers.
These objects cannot be recorded to directly, but need to be filled with commands through an ISubCommandBuffer object.

The commands recorded here are used to make actual draw calls, which execute the graphics pipeline.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[draw\|IRecordingSubCommandBuffer::draw]] | Perform draw call |
| [[drawIndexed\|IRecordingSubCommandBuffer::drawIndexed]] | Perform draw call with index buffer |
| [[setVertexBuffer\|IRecordingSubCommandBuffer::setVertexBuffer]] | Set vertex buffer to use |
| [[setIndexBuffer\|IRecordingSubCommandBuffer::setIndexBuffer]] | Set index buffer to use |
| [[setDynamicIndex\|IRecordingSubCommandBuffer::setDynamicIndex]] | Records the binding of which index in a IDynamicBuffer to use. |