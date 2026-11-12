# Pixel_Arts256x128

The pictures for the Pixlpal Digital Art app's gallery. The device downloads each one from this folder when it is
shown, without a token, so this repository must stay public.

## Adding pictures

- PNG files, 256×128 pixels, directly in this folder (not in a subfolder).
- The gallery asks only for the names it was built with: the `names` list in the firmware's
  `components/All_Open_Pxp_Apps/Meterbit_Apps/App_Meterbit_Digital_Art/include/mtb_pixel_art_png.h` (634 names).
  A file must use one of those names exactly, including capitals and spaces. A picture with any other name is never
  shown, and a listed name with no file here fails to download.
- To add a new name, add it to that list and release new firmware.

The repository and folder are set in the firmware's menuconfig, under "Pixlpal asset downloads"
(`CONFIG_PXP_ASSETS_GITHUB_REPO`, `CONFIG_PXP_ASSETS_PIXEL_ART_FOLDER`).
