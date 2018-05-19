defined in header `"parser.hpp"`

`class Parser;`

The Parser class reads and compiles GLSL files into SPIR-V binaries, used by Vulkan.
It also reads the bindings used in the shaders and stores them for later when used to assign data to those bindings, and the format of the input buffer.

This means that the vertex buffer used must match the layout of the data in the shader, or it will give unpredicted results.

Note that GLSL creates padding between data so that it is 64 aligned by bytes per default.
64 bytes is enough room for one 4x4 matrix of floating points.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[(constructor)\|Parser::Parser]] | constructs a parser
| [[compileVertexShader\|Parser::compileVertexShader]] | Compiles a .vert file (written in GLSL) into byte code|
| [[compileFragmentShader\|Parser::compileFragmentShader]] | Compiles a .frag file (written in GLSL) into byte code |