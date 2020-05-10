# volumio_keyboard
Virtual Keyboard to use with official 7" touch screen

login: volumio
password: volumio

After you have installed the touch screen plugin.

On the command line or by via SSH install the following:
sudo apt-get install matchbox-window-manager matchbox-keyboard

Edit the following file:
sudo nano /opt/volumiokiosk.sh
It'll ask for password

comment out the line:
openbox-session &

then add the following underneath your #openbox-session &:
matchbox-keyboard -d &
matchbox-window-manager -use_titlebar no &

save it by pressing Ctrl + x, press y then enter.

NEXT:

Backup the default keyboard file keyboard.xml by:
cd /usr/share/matchbox-keyboard/
sudo mv keyboard.xml keyboard.xml_old

whilst your in this directory copy the keyboard.xml file in this repository and save it in your current directory.

reboot your raspberry pi and it should work ok.

Touch the search box to bring up the keyboard enter your search details and volumio will automatically search then touch outside of keyboard to view your searched music.
