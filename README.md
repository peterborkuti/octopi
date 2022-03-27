## Install CUPS with Octopi on Raspberry pi and use your old HP printer

Install OctoPi using the Raspberry Pi Imager:
https://octoprint.org/download/

When you set-up, enable SSH with password. This is important,
because you will need sudo, and suo needs password.

When installing done, log in to pi:

```
ssh pi@your.octopi.ip

sudo apt-get update
sudo apt-get upgrade

sudo reboot
```
connect your old HP usb printer

```
ssh pi@your.octopi.ip

sudo apt-get install cups
sudo usermod -a -G lpadmin pi
sudo cupsctl --remote-any

sudo apt-get hplip
sudo hp-plugin -i
```

If everything goes well, it will download and install a firmware file for your old HP printer.
You will notice, that the printer's motor will start for a short time.

Go to http://your.octopi.ip:631
Add your printer 
* it will ask for the login password, login is "pi" the password is what you gave when setup
raspberry imager
* Do not forget to check Share 
* Print a test page


## Setup printer from remote Linux

Simply add printer, it will find if you are on the same network.

## Setup printer from remote Windows

See the end of this guide:
https://www.tomshardware.com/how-to/raspberry-pi-print-server





