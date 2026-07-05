# Hannah Montana Linux v26
![Preview of Hannah Montana Linux](https://gitlab.com/DecaCagle/hannah-montana-kde-theme/-/raw/master/look-and-feel/com.decacagle.hml/contents/previews/fullscreenpreview.jpg?ref_type=heads)
---
Hannah Montana Linux v26.0 is a modern remaster of the [original Hannah Montana Linux](https://hannahmontana.sourceforge.net/). It uses Debian's [live-build](https://live-team.pages.debian.net/live-manual/html/live-manual/index.en.html) and the [Calamares installer](https://calamares.io/).

Much of this project is just a re-skin of [KDE Plasma](https://kde.org/plasma-desktop/). Many of the Plasma components are direct modifications of Plasma's default theme, [Breeze](https://github.com/kde/breeze). As such, this project is licensed under **GPLv3+**.

This project was made as the focus of a video on my [YouTube channel](https://www.youtube.com/@noah-cagle). You can watch the video [here](https://www.youtube.com/watch?v=VKx5UZsX9jw).

## Note: If you need a distro for old hardware, check out [HML26 Lite](https://gitlab.com/DecaCagle/HannahMontanaLinux26Lite)
The main project uses KDE Plasma 6 and SDDM. Plasma 6 can be sluggish on older machines. **Generally, you need about 8GB of RAM to run Plasma 6 comfortably**. However, [HML26 Lite](https://gitlab.com/DecaCagle/HannahMontanaLinux26Lite) is a fork of this project that uses [LXQt](https://lxqt-project.org/) and [lightdm](https://github.com/ubuntu/lightdm) instead. **LXQt can run comfortably with only 2GB of RAM, while offering a fully capable desktop experience.** It's certainly not as pretty as Plasma 6, but it's a hell of a lot more efficient.

## Download the latest ISO from the [releases page](https://gitlab.com/DecaCagle/hannahmontanalinux26/-/releases)

However, if you'd prefer to build the project from source rather than using the pre-built ISO, you can do so easily.

## __Build from source__
**Requirements:**
Install live-build from the apt repository:
```
sudo apt install live-build
```

**Note:** live-build requires a Debian-based system. It will not work on other Linux distributions, not even inside of a Docker container (I tried).

__**Steps to build ISO**__
Clone this repository and navigate to it:
```
git clone https://gitlab.com/DecaCagle/HannahMontanaLinux26 && cd HannahMontanaLinux26
```

Run the live-build pre-configuration command:
```
lb config
```
Note: There is an executable script inside of the 'auto' directory called 'config'. If you have issues, make sure this file *is indeed executable*. When there is a config script in the 'auto' directory, live-build will automatically run *that* script when `lb config` is run.

Build the project with sudo:
```
sudo lb build
```
Note: This will take quite a while to complete. On my system, it takes around 10 minutes. It's also prone to eat up a lot of memory, so I recommend you close as many background apps as you can before building.

Once the build is completed successfully, you will find an ISO titled `live-image-amd64.hybrid.iso` at the root of the repository.
