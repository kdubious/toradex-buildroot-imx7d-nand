# toradex-buildroot-imx7d-nand
Setup for using Buildroot with the Toradex iMX7D 512MB NAND SoM

This is not intended to be a Buildroot tutorial, so these steps assume you have read the Buildroot docs

1. Download a copy of Buildroot, extract to a local folder. (Or clone with git)

The details here assume that Buildroot is located at `~/buildroot`

2. Clone this repo. (Or Fork it, then clone it)

The details here assume that this repo is located at `~/toradex-buildroot-imx7d-nand`

3. `cd ~/buildroot`

4. In the Buildroot folder, set up for keeping customizations outside of Buildroot:

(https://buildroot.org/downloads/manual/manual.html#outside-br-custom)

`make BR2_EXTERNAL=~/toradex-buildroot-imx7d-nand/colibri nconfig` (nconfig, or menuconfig, or xconfig, etc.)

5. Save and Exit

6. You can now run `make toradex-defconfig`, which is in this repo

7. `make nconfig` (nconfig, or menuconfig, or xconfig, etc.)

8. Add packages and change settings as you wish

9. `make clewan all`

10. Wait. Now you have the assets in `~/buildroot/output/images` for a TEZI install. Update your image.json as needed

https://developer.toradex.com/software/toradex-easy-installer

a. UBOOT

b. KERNEL

c. DTB

d. RootFS



