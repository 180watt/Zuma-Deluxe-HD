# Zuma-Deluxe-HD-24

## Fork Info
This should compile on any reasonable platform. (OK, probably not windows, but if that's the case- please, report a bug.)
Anyhoo, you'll probably still need to change the `CMakeLists.txt` file to search in the proper paths for your system.
With the transfer to `SDL_mixer`, some things have been lost. Namely, the fact that `SDL_mixer` can only play the first
track of the "OST", so that's the music for the whole game. (Looking into this.) Secondly, `SDL_mixer` doesn't support pitch
shifting natively, so until I stop being lazy, we don't have pitch shifting either.

A remake of the legendary 2003 PopCap game with improved textures and support for 16:9 aspect ratio. Made by me and [s4lat](https://github.com/s4lat).

![preview](https://user-images.githubusercontent.com/52833080/162574925-d6c9f657-c2e4-43e3-860d-412e60f14834.png)

## [Gameplay video on YouTube](https://www.youtube.com/watch?v=VZYsNUUAozM&ab_channel=GalaxyShad)

## 🎥 Media 
![Zuma_Deluxe_HD_Remake](https://github.com/GalaxyShad/Zuma-Deluxe-HD/assets/52833080/a84a71f4-385a-4d01-b4ce-b9ccf47d6f85)
![Zuma_Deluxe_HD_Remake (1)](https://github.com/GalaxyShad/Zuma-Deluxe-HD/assets/52833080/a006a96f-805f-46d1-ac8f-340524df3cdd)

## Direct link to download the latest build
 [⬇️ [Stable] ZumaHD v0.1.0 Windows.zip ](https://github.com/GalaxyShad/Zuma-Deluxe-HD/releases/download/v0.1.0/zuma-hd-v0.1.0-windows.zip)

## ⛓️ Dependencies
* [SDL2 	   2.26.5](https://www.libsdl.org)
* [SDL2_image 	2.6.3](https://www.libsdl.org/projects/SDL_image)
* SDL2_mixer
* [Expat 		2.5.0](https://github.com/libexpat/libexpat)

## 🛠️ Build via CMake
```
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
cd bin
./ZumaHD
```

## 🔗 Sources used
Thanks to [hclxing](https://hclxing.wordpress.com/2017/06/27/reverse-engineering-zuma-deluxes-level-file/) for the article on how paths are stored in .dat files.

## 📃 License 
Source code is under MIT License, but all assets (in content folder) belong to [PopCap and EA games](https://www.ea.com/ea-studios/popcap)

## 10.04.2023 Status
Currently project framework is under reconstruction, check ["api-rework" branch](https://github.com/GalaxyShad/Zuma-Deluxe-HD/tree/api-rework).
