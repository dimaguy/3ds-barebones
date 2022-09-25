# 3ds-barebones
A template for homebrew development on the 3DS using devkitarm

## Getting started
1. Follow the [dkp-pacman installation guide](https://devkitpro.org/wiki/devkitPro_pacman)
2. Install the 3ds-dev group of packages (`sudo dkp-pacman -S 3ds-dev`)
3. Start coding!

To compile, read and tweak the provided makefile and it will produce 3dsx, elf and (optionally) smdh files.

Tip: Use `3dslink` to quickly get your 3dsx loaded on your 3DS

## How to create CIA files?
CIA files aren't just a direct packaging of 3dsx files on an installable format, they bundle a lot of the data needed to work in them, and as such you have to provide the following files:
1. A RSF file to set the rules and specifications of the app.
2. A 48x48 PNG image to create a home menu icon for your app.
3. A 256x128 PNG image to create a home menu banner for your app.
4. (OPTIONAL) A WAV/OGG file to serve as home menu sound for the app. (Must be at most 3 seconds to avoid issues)

You will also need [`bannertool`](https://github.com/Steveice10/bannertool/releases/tag/1.2.0) to generate the bnr(banner) and a icn(icon) file and [`makerom`](https://github.com/3DSGuy/Project_CTR/releases/tag/makerom-v0.18.3) to generate the CIA file after you've gathered all the needed components.

Tip: Create a 1280x640 image to serve as social media preview of your repository.
