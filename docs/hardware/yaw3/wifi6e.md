# Upgrade Yaw 3 to Wifi 6E

The Image below has a more recent version of RaspberryPi OS than the image supplied with your chair, and I had to redevelop portions of the Yaw software to work with changes in the OS, I also added some performance improvements!

Prior to doing this you should execute the following on the chair:

SSH into the device, substitute with the IP of your simulator on your network:

`ssh pi@192.168.0.120` The password is pi

Then execute the following command and store the output:
`sed -n 's/^License=//p' /usr/local/etc/virtualhere/config.ini`

The output is your VirtualHere license, save this! you will need this if your SD ever gets corrupted and you need to reflash the SD, without it you will probably need to re-purchase VirtualHere, as long as you have this you can relicense VH on the same physical Raspberry Pi.

## Whats required

- [RPI PCIE Adapter board (MPW7N)](https://s.click.aliexpress.com/e/_oBgVflp)
- [AX210NGW Nic (AX210 10dbi Kit)](https://s.click.aliexpress.com/e/_oBzd06B)
- [Longer PCIE ribbon](https://amzn.to/4oOFzo0)
- [3D Printed mounting adapter, STL here](../../assets/3dmodels/yaw3-hat_mount.stl)

Flash the following image to SD card using <a target="_blank" href="https://etcher.balena.io/">Balena Etcher</a>

<a target="_blank" href="https://www.dropbox.com/scl/fi/e9qmyjaa4kf5834dsfl0g/YawIII-RaspberryPIOS12-wifi6E-opt.zip?rlkey=uhi4oinz3wbrz24ghkpc9n4go&st=gc2d5hpm&dl=0">YawIII-RaspberryPIOS12-wifi6E-opt.zip</a>

## How to install it

<video width="1280" height="720" controls>
  <source src="/assets/video/yaw3wifi6e.mp4" type="video/mp4">
Your browser does not support the video tag.
</video> 

## This took a few months to figure out. I also had to rebuild the entire image and redevelop the Yaw software to work with newer RaspberryPi OS. If it helped you.. maybe you could  
<div align="center">
<script type="text/javascript" src="https://cdnjs.buymeacoffee.com/1.0.0/button.prod.min.js" data-name="bmc-button" data-slug="ItsVRK" data-color="#FFDD00" data-emoji="" data-font="Cookie" data-text="Buy me a coffee" data-outline-color="#000000" data-font-color="#000000" data-coffee-color="#ffffff" ></script>
</div>