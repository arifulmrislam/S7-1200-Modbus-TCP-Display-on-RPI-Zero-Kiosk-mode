# S7-1200-Modbus-TCP-Display-on-RPI-Zero-Kiosk-mode

1.Memory card prepare:

•	Firstly, format memory card by application.

•	Then download the Raspberry pi0-light.

•	Setup operating system by balenaEtcher.

•	After preparing everything set the memory card in RPI0.

2.Setup RPI0 fully for kiosk Mood:

1.	For back to main file, Alt+Ctrl+F3/F1

2.	For shutdown, sudo shutdown -h now

Login-pi
Password-123456

$sudo raspi-config

$sudo apt-get update

$sudo apt-get install --no-install-recommends xserver-xorg x11-xserver-utils xinit openbox

$sudo apt-get install --no-install-recommends chromium-browser

$sudo nano /etc/xdg/openbox/autostart

$xset -dpms			# turn off display power management system

$xset s noblank		# turn off screen blanking

$xset s off			# turn off screen saver

$startx

$source .bash_profile

[[ -z $DISPLAY && $XDG_VTNR -eq 1 ]] && startx

$sudo reboot

How do I disable Restore pages? Chromium didn't shut down correctly. Prompt?

I've got it! Use --app=your.url

For example:

chromium-browser --kiosk --app=http://your.url.here

🚩 Connect with me on social
- LinkedIn: [LinkedIn](https://www.linkedin.com/in/ariful-islam-arif-2987b51a3/)
- Twitter: [Twitter](https://twitter.com/arifulislam301)
- Instagram: [Instagram](https://www.instagram.com/ariful_mr_islam/)

🔔 Subscribe to my YouTube channel: [YouTube](https://www.youtube.com/channel/UCED68cm6nHaAlAk0h9I3yAQ)


