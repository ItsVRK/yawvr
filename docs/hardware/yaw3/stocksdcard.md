# Update or restore SD Card for Yaw 3

This stock image has a more recent version of RaspberryPi OS, and I had to redevelop portions of the Yaw software to work with changes in the OS, I also added some performance improvements!

If you want to modify the chair to support [Wifi6E then skip to here](wifi6e.md)

Prior to doing this you should execute the following on the chair:

SSH into the device, substitute with the IP of your simulator on your network:

`ssh pi@192.168.0.120` The password is pi

Then execute the following command and store the output:
`sed -n 's/^License=//p' /usr/local/etc/virtualhere/config.ini`

The output is your VirtualHere license, save this! you will need this if your SD ever gets corrupted and you need to reflash the SD, without it you will probably need to re-purchase VirtualHere, as long as you have this you can relicense VH on the same physical Raspberry Pi.

## Updated RaspberyPi OS Stock Image

Flash the following image to SD card using <a target="_blank" href="https://etcher.balena.io/">Balena Etcher</a>

<a target="_blank" href="https://www.dropbox.com/scl/fi/z3sw98az1iv9dd7d81ekb/YawIII-RaspberryPIOS12-clean-opt.zip?rlkey=op915xaa90l3ocizqkcvj2ovu&st=o4hwm8b4&dl=0">YawIII-RaspberryPIOS12-clean-optimized</a>

**Note:** Some users have had issues connecting via bluetooth to send wifi details to work around this do the following.

Connect ethernet cable to the Pi, ssh into the pi and execute the following, replacing `AccessPointName` with your actual AP's name in both lines and `***` with the wifi password in the first line:

```
sudo nmcli dev wifi connect "AccessPointName" password "***" ifname wlan0
sudo nmcli connection modify AccessPointName connection.autoconnect yes
```

Then you can execute `sudo reboot` in the terminal and unplug ethernet while it's rebooting, it should connect to wifi automatically now.


## I had to rebuild the entire image and redevelop the Yaw software to work with newer RaspberryPi OS. If it helped you.. maybe you could  
<div align="center">
<script type="text/javascript" src="https://cdnjs.buymeacoffee.com/1.0.0/button.prod.min.js" data-name="bmc-button" data-slug="ItsVRK" data-color="#FFDD00" data-emoji="" data-font="Cookie" data-text="Buy me a coffee" data-outline-color="#000000" data-font-color="#000000" data-coffee-color="#ffffff" ></script>
</div>