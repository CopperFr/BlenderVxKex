# BlenderVxKex

Windows 7 CUDA & OptiX support for Blender 4.x and newer with [VxKex](https://github.com/CopperFr/VxKex).

## Description

This repository contains releases of files to replace in the official portable install
of Blender to have CUDA and/or OptiX cycles working when [VxKex](https://github.com/CopperFr/VxKex) is used.

Build environment:
```
Visual Studio 2019, version 16.11.53
Windows SDK 10.0.22621.0
NVIDIA CUDA 10.2 / 11.8 
NVIDIA OptiX 7.3
```
When you use [VxKex](https://github.com/CopperFr/VxKex) on the official portable install of Blender it will work but cycles
CUDA or OptiX will not. For CUDA you'll have an error:
**Failed to load CUDA kernel from '...\kernel_sm_XX.cubin.zst' (Invalid kernel image)**

It will work if you replace files from **blender-CUDA-OptiX-patch_4_x_x.zip** but you will still
need to use [VxKex](https://github.com/CopperFr/VxKex).

For CUDA you can only replace the file indicated in the error message.

For OptiX you need to replace other files and blender.exe because official one is checking for r535+ drivers to enable OptiX.  
(OptiX 8.0 requires that you install a r535+ driver not available in Windows 7)

**Support is only available for compute capability between 3.0 and 8.9.**  

more about CUDA: https://en.wikipedia.org/wiki/CUDA

OptiX cycles is not working correctly when Open Shading Language is checked
