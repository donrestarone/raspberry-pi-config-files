#general setup
in the terminal type:
```
sudo raspi-config
```
you can enable ssh here. Or you can add a .ssh file to root of the boot sd card


## to disable swap
```bash
sudo dphys-swapfile swapoff && sudo dphys-swapfile uninstall && sudo systemctl disable dphys-swapfile
```
after disabling swap. output of 
```bash
free -h
```
should be 
```bash
Swap:            0B          0B          0B
```

## Disable HDMI/video 
```bash
fbset -xres 16 -yres 16 -vxres 16 -vyres 16 -depth 8
```
```bash
/opt/vc/bin/tvservice -o
```
