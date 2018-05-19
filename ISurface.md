defined in header `"isurface.hpp"`

`class ISurface;`

ISurface is an interface class for creating surfaces. The API does not support window creation, which means that the developers must create a window first and then make a surface with it. At the moment we only support surface creation with Win32 windows.

## Methods
| Methods  | Description |
| ------------- | ------------- |
| [[getWidth\|ISurface::getWidth]] | Returns the width of the surface |
| [[getHeight\|ISurface::getHeight]] | Returns the height of the surface |
| [[createWin32Surface\|ISurface::createWin32Surface]] | Creates a Window Surface of type Win32 |