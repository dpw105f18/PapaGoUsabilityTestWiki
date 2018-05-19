defined in header `"icommand_buffer.hpp"`

`class ISubCommandbuffer;`

Objects of this class are used to record GPU commands into a IRecordingSubCommandBuffer object.
This is the only way to record commands into a ISubRecordingCommandBuffer.
This type of command buffer cannot be executed directly on a queue, instead it is executed as part of an ICommandBuffer. 
These are the only command buffers, which can be recorded to in parallel.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[record\|ISubCommandBuffer::record]] | Records commands into a IRecordingSubCommandBuffer|