# razer-blade-15-linux-config
Some configuration files for running a razer blade 15 on linux. Configurations have been tested on Manjaro Linux.

# Touchpad configuration
Seems like the synaptics driver works best. You can have kinetic scrolling and pixelwise scrolling. The config is mac-like, i.e. two finger scrolling, taps are disabled, speed and acceleration feel natural. Install the driver and copy 
70-synaptics.conf to /etc/X11/xorg.conf.d/

# Chromium configuration
Enables two finger history back and next overscroll and activates some hardware acceleration
`cp  chromium-flags.conf ~/.config/`

# Set keyboard chroma
Install openrazer and run the keyboard_chroma.sh shell script to get green keys except red arrow keys. Note that you might need to adjust $dev to match your keyboard device.
To start it automatically copy keyboard.desktop to ~/.config/autostart/ (and ajust the path in keyboard.desktop to keyboard_chroma.sh)

# NVidia Optimus
Install optimus-manager, linuxXX-bbswitch, linux-nvidia and copy the optimus-manager.conf to /etc/optimus-manager and enjoy   (idle) energy consumption below below 10 W and 8 hours and more "time to empty".

# Fix resume after suspend
add `button.lid_init_state=open` to `GRUB_CMDLINE_LINUX_DEFAULT` in `/etc/default/grub` and update grub

# Terminal font size
copy vconsole.conf to /etc/vconsole.conf and enjoy a readable console font size.
