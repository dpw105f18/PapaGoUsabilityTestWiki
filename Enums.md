Defined in header `"api_enums.hpp"`

Below we describe all global enums, which are avaliable.

## Format
Used to set the format of color and depth/stencil buffers.

| Enum Name  | Description |
| ------------- | ------------- |
| eR8G8B8Unorm | Three 8 bit color channels in the following order; Red, Green, Blue of unsigned normalized floats. |
| eR8G8B8A8Unorm | Four 8 bit color channels in the following order; Red, Green, Blue, Alpha of unsigned normalized floats.|
| eB8G8R8A8Unorm | Four 8 bit color channels in the following order; Blue, Green, Red, Alpha of unsigned normalized floats.|
| eS8Uint| A single channel with 8 bit unsigned integer |
| eD32Sfloat| A single channel with 32 bit float |
| eD32SfloatS8Uint| Two channels in the following order: 32 bit float 8 bit unsigned integer  |
| eD24UnormS8Uint| Two channels in the following order: unsigned normalized float, unsigned integer |

## Filter
Defines filtering in a sampler

| Enum Name  | Description |
| ------------- | ------------- |
| eNearest | Nearest neighbour filtering |
| eLinear | Linear interpolation filtering |

## TextureWrapMode
Defines texture wrapping in a sampler

| Enum Name | Description |
| ------------- | ------------- |
| eClampToBorder | clamp to border wrap mode |
| eClampToEdge | clamp to edge wrap mode |
| eMirroredRepeat | mirrored repeat wrap mode |
| eMirrorClampToEdge | mirror clamp to edge wrap mode. Only supported if VK_KHR_sampler_mirror_clamp_to_edge extension is enabled on device |
| eRepeat | repeat wrap mode |