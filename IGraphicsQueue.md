defined in header `"igraphics_queue.hpp"`

`class IGraphicsQueue;`

IGraphicsQueue is an interface to the queue used by the GPU.
To execute the commands stored in an ICommandBuffer, it must be submitted for execution on the queue.
Thus, the commands recorded have no effect before being executed on the queue.
This however allows the command buffers to be reused across many different frames, which combats CPU-boundness.


## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[submitCommands\|IGraphicsQueue::submitCommands]] | submit commands to the graphics queue and execute them |
| [[present\|IGraphicsQueue::present]] | present the current framebuffer |
| [[getLastRenderedImage\|IGraphicsQueue::getLastRenderedImage]] | get access to the color buffer rendered to last|
| [[getLastRenderedDepthBuffer\|IGraphicsQueue::getLastRenderedDepthBuffer]] | get access to the depth buffer rendered to last|


