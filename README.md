# optimus-indicator

A simple indicator for Optimus Laptop.

It shows the bumblebee icon if bumblebee is in use, the NVIDIA icon if Xorg was started with `nvidia-xrun` or the Intel icon if the NVIDIA dGPU is turned off.

It was meant to be used with both `bumblebee` and `nvidia-xrun` on Debian.

If you are interested in this kind of configuration you may like my other projects [nvrun](https://github.com/ferdiu/nvrun) and [nvidia-xorg](https://github.com/ferdiu/nvidia-xrun) meant to be used with this setup.

## Structure
* **optimus-indicator** - uses following dir structure:
* **/usr/bin/optimus-indicator** - the executable python3 script
* **/usr/lib/optimus-indicator/icons/intel.svg** - the icon for gGPU turned off
* **/usr/lib/optimus-indicator/icons/bumblebee.svg** - the icon for gGPU turned on using `optirun`/`primusrun`/`nvrun`
* **/usr/lib/optimus-indicator/icons/nvidia.svg** - the icon for gGPU turned on and used by Xorg
* **/usr/lib/optimus-indicator/check-gpu** - a script to check if NVIDIA card is turned on
* **/usr/lib/optimus-indicator/check-nvidia-method** - a script to check if NVIDIA card was waked by `bumblebee` or `nvidia-xrun`

**NB** You can install `optimus-indicator` script anywhere but the other files need to be in the direcory `/usr/lib/optimus-indicator/`.

## DEB Package
The Debian package (not tested on other distros) can be downloaded [here](https://ferdiu.github.io/debs/optimus-indicator_0.1-1.deb).
