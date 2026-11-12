# Pixel_Arts256x128

The pictures for the Pixlpal Digital Art app's gallery. The device downloads each one from this folder without a
token, so this repository must stay public.

## Adding pictures

- Put `.png`, `.jpg` or `.jpeg` files directly in this folder (not in a subfolder). Every one is in the gallery:
  no list to edit and no new firmware.
- 256×128 pixels fills the panel. A smaller picture is enlarged by a whole factor (128×64 shows at twice its size).
  JPEGs must be baseline, not progressive.
- The phone shows a title made from the file name: `a-cozy-sitting-room.png` becomes "A cozy sitting room". Use
  dashes or underscores between words.
- Devices read this folder's list when Digital Art first starts and then every 6 hours, so a new picture can take
  up to 6 hours to appear on a device that is already running (restarting the device shows it sooner).
- GitHub lists at most 1,000 files in a folder, which is also the gallery's limit.

The repository and folder are set in the firmware's menuconfig, under "Pixlpal asset downloads"
(`CONFIG_PXP_ASSETS_GITHUB_REPO`, `CONFIG_PXP_ASSETS_PIXEL_ART_FOLDER`).
