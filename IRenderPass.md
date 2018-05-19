defined in header `"irender_pass.hpp"`

`class IRenderPass;`

IRenderpass encapsulates a render state, including shaders which are set at construction and parameter bindings, which can be changed during the object's lifetime. Every command submitted to the GPU is associated with such an object. 

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[ bindResource\|IRenderPass:: bindResource]] | submit commands to the graphics queue and execute them |
