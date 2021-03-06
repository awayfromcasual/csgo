# My Counter-Strike Settings

These are my Counter-Strike settings. To use my custom .cfg files, go to where Steam is installed and copy the contents of the `cfg` and `modes` directories into one of two cfg folders:

- `\...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg`
	- This folder is where Steam stores most of the configurations for different gamemodes (competitive, casual, deathmatch, etc), as well as the default config. I prefer using this folder because it is shared between accounts.
- `\...\Steam\userdata\<your steam id>\730\local\cfg`
	- This folder is where Steam stores your config.cfg and video.txt files. Most guides suggest using this folder because this is where your configuration files are stored.

Once the files are copied, to use the commands in _commands.cfg, either add `exec _commands` to your launch options, or use a cumulative `_launch.cfg` as I explain below.

## Files

Here is a list of the files in this repository:

- `_autoexec.cfg` - This is my autoexec. It contains all of my personal settings (binds, sensitivity, crosshair, etc).
- `_commands.cfg` - This containes bindable aliases like the jumpthrow script, and shortcuts for using console commands like clear, disconnect, and quit.
- `_launch.cfg` - This is a file I use to manage commands I want executed on launch, like `exec _commands`, which loads all my custom aliases. I use a dedicated .cfg file for this to avoid clogging the Steam launch options box.
- `_1v1-ak.cfg` - Config file for setting up a 1v1 server where the default weapons are AKs and deagles.
- `_1v1-default.cfg` - Config file for setting up a 1v1 server.
- `_practice.cfg` - Config file for setting up a practice server (max money, infinite ammo, grenade trajectory, etc).

## Launch Options

Open Steam, go to your library, right click on CS:GO, and click "Properties". Launch options are entered in the box at the bottom of the "General" tab.

Here are my launch options: `-high -nojoy -novid -d3d9ex -tickrate 128 +exec _launch`

### Important launch options:

- `-novid` - Disables the intro, which makes loading the game faster.
- `-d3d9ex` - Makes alt-tab instantaneous. Might also improve FPS.
- `-tickrate 128` - Sets the tick rate for local servers to 128 instead of the default 64.

### FPS boosting launch options:

Some people (including myself) find FPS improvements with the following launch options:

- `-high` - Sets CS:GO to run at high priority, which may improve FPS.
- `-nojoy` - Disables joystick support, which may improve FPS.

### Using a dedicated launch.cfg file:

Many guides suggest using `exec autoexec` so your settings always reset when you launch the game. I prefer to use a separate `_launch.cfg` file, which only includes commands that I want reset every launch (cl_crosshaircolor, fps_max, r_dynamic, etc). This lets me change settings without them resetting every time I restart the game. Some commands (r_dynamic in particular) have to be executed on launch or they will reset to the default value.

- `+exec _launch` - Executes my launch options file.

## Graphics Settings

Here are my video settings:

	Color Mode:                             COMPUTER MONITOR
	Brightness:                             80%
	Aspect Ratio:                           WIDESCREEN 16:9
	Resolution:                             2560X1440
	Display Mode:                           FULLSCREEN
	Laptop Power Savings:                   DISABLED

	Global Shadow Quality:                  MEDIUM
	Model / Texture Detail:                 HIGH
	Texture Streaming:                      DISABLED
	Effect Detail:                          LOW
	Shader Detail:                          HIGH
	Boost Player Contrast:                  ENABLED
	Multicore Rendering:                    ENABLED
	Multisampling Anti-Aliasing Mode:       2X MSAA
	FXAA Anti-Aliasing:                     DISABLED
	Texture Filtering Mode:                 ANISOTROPIC 16X
	Wait For Vertical Sync:                 DISABLED
	Motion Blur:                            DISABLED
	Triple Monitor Mode:                    DISABLED
	Use Uber Shaders:                       AUTO: ENABLED

These video settings are not optimized for visibility. These are just the settings that I prefer to use. If you are interested, here are some videos that explain the optimal settings for in-game visibility:

[ALBU Performance's Settings Benchmark](https://www.youtube.com/watch?v=e2e26BGdPxk)

[MrMaxim's 2022 CS:GO Setup Guide](https://www.youtube.com/watch?v=_NDlFy-Mc5Q)

[Voo's 2021 GS:GO Settings Guide](https://www.youtube.com/watch?v=aqTLaUDGPiM)

## Simple Radar

I also use an add-on called Simple Radar. Simple Radar a customization that replaces the default radar with an improved radar that is more accurate and easier to read. It also just looks more modern than the default CS:GO radar.

[Simple Radar 5.2](https://readtldr.gg/simpleradar-download) (Password: **gooseman**)

To use Simple Radar, copy the files from the download into this folder:

`\...\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\resource\overviews`

## FPS Fix

If you're having FPS drops, this might help:

- Go to Steam -> Settings
- Go to Web Browser
	- Delete cache
	- Delete cookies
- Go to Downloads
	- Clear download cache
- Restart Steam
