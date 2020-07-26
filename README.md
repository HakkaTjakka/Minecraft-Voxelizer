# Minecraft-Voxelizer

https://www.youtube.com/watch?v=mHpsJtditZ4&list=PLetXkEBOuSmbMy6o2PPLpZrrcPwjw3K4W&index=18

Convert Wavefront 3d objects (.obj/.mtl/textures) to Minecraft region (1.12.2 .mca) and/or schematic (WorldEdit) files.

For c/c++ programmers only. But also works from command line and/or graphical interface.

Creates hundreds of thousands of blocks per second from 3d objects. 
Used to voxelize 3d objects from Google Earth 3d (whole cities).
Could be used for BUILD THE EARTH 1TO2 project. (Building whole earth on 1 to 1 scale, 1 block = 1 cubic meter)

Usage:

Download/Setup/Install https://github.com/HakkaTjakka/MinecraftWorldEditor
(Not all is needed..., the total is user nightmare, but everything works, when knowing how...)
Directory for models, with each model in sep. dir, plus run makelist.bat for making list.txt with all the paths to all objects.

Important files to watch:
  pacman.ini
  pacman_cuberite/src/viewer/*.*        (reading/displaying/converting 3d .obj files)
  pacman_cuberite/src/mceditor/test.c   (create region (.mca) files)
  pacman_cuberite/src/wuppie.cpp        (voxelizer, works with /src/viewer/*.* files)

Create schematic 100 blocks high (automatic from command line)

  schematic "skull\skull.obj" auto 100

Adjust size/rotation with mouse (by hand within program) 

  schematic "formula_1\Formula_1_mesh.obj"
  
  Mouse: Left -> Rotate,  Right -> Size
  REGIONS:F1 voxelize, CTRL-F1 finish them all to region files
  SCHEMATIC: SHIFT-F1 Create schematic from object (destroys F1 made...)
  CTRL+SHIFT-F1 Create schematic from object plot with F1
  CTRL+SYSTEM+SHIFT + left/right prev/next model (see ../models/list.txt)
  CTRL+SHIFT + left|right ADD prev/next model
  ANGLES: ALT + left|right|up|down|pgup|pgdn rotate x/y/z
  QUATS: CTRL + left|right|up|down|pgup|pgdn rotate x/y/z
  F5 Text on/of  F6|F7|F8 reset view
  ALT-F6|ALT-F7|ALT-F8 reset angle x|y|z
  F11 Full screen / window
  SHIFT-F5 Round Angles(1)  SHIFT-F6(5)  SHIFT-F7(10)  SHIFT-F8(90)
  ALT-F1 Plot regions on canvas window  DELETE Clear voxels (from F1)
  CANVAS WINDOW: ALT+DEL(3x) Clear screen  SHIFT-D foreground/background screen
  F2: WRITE REGION.VOX VOXEL FILES TO REGION.MCA FILES  CTRL-F2: FLUSH VOXELS TO REGION VOXEL FILES
  SHIFT-F2: PLOT REGION.VOX VOXEL FILES
  F10: Rotate on  ALT-F10: Plot when rotate on
  CTRL+ALT+ LEFT/RIGHT: Load and add next/prev object to current.
  CTRL+SYSTEM+ALT+ LEFT/RIGHT: Load next/prev object.
  CTRL-Q: close window.

  For other keys see src/viewer/my_viewer_events.hpp
  (Lots of .hpp files make viewer_my.cpp, in fact its one long .cpp file)
  
Code is a nightmare. Reverse engineer and/or msg me for help on whatever. (Installing compiler / codeblocks / program / ffmpeg / usage)
Its a preliminary experimental prototype machine, whith all sorts of code that is missing on the net.
Collection of lots of other GitHub sources.

Thanks to all programmers on GitHub for several parts of the code, like for .nbt writing/reading, .mca creation, region file writing, 3d rendering, sfml, etc. etc.
The program is like the Frankenstein monster, who is made from several bodyparts from several (dead ... ;) ) bodies. Then it comes alive.

https://www.youtube.com/watch?v=b4Oge1YJjvI&list=PLetXkEBOuSmbMy6o2PPLpZrrcPwjw3K4W
https://www.youtube.com/watch?v=kXZ8LpmC2yU&list=PLetXkEBOuSmaP0O9firbuT9lHcn25QuiW

Wanted:

People who want to make a nice Minecraft tool out of the source.
