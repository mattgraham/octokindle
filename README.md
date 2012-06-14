Octokindle
==========
------

These modifications should work with the v5.1.0 firmware version of Kindle Touch. Make all changes at your own risk. (It was a very smooth install for myself) I am just the screensaver orginizer if you have any questions hit me up on twitter: [@michigangraham](http://twitter.com/#!/michigangraham).

Huge thanks to [@cobyism](https://github.com/cobyism) and [@dreww](https://github.com/dreww) for getting things rolling on this, much of this content is from/because of them.

Feel free to submit pull requests with new octocat screensavers. I'll accept and reject them based on my personal biases, and taste in design.

![Octokindle](http://distilleryimage11.s3.amazonaws.com/39668d96b56c11e1abb01231382049c1_7.jpg)

## Removing Advertisements

There are ways on the interweb to remove the advertisements from your kindle. Hoevere, my recomendation is, pay for them. Goto "Manage Your Devices" tab in your amazon account and unsubscribe from special offers. Its anoying I understand, but the right thing to do. 

## Jailbreak

In order to do nifty things with your Kindle, you'll need to jailbreak it first. On it's own, this doesn't do anything, however, it will allow beautiful customizations to happen.

1. Download [the jailbreak file](http://gr4m.com/LAmdhG)
2. Plug in the Kindle via USB and copy all the files and directories contained in the downloaded zip file (data.tar.gz, ENABLE_DIAGS, diagnostic_logs) directly to the Kindle’s USB drive’s root.
3. Safely remove/eject the Kindle from USB and restart it (Menu -> Settings -> Menu -> Restart)
4. Once the device restarts into diagnostics mode, select "D) Exit, Reboot or Disable Diags" (by tapping on the appropriate entries)
5. Select "R) Reboot System" and "Q) To continue"
6. You should see the Jailbreak screen and the device should restart back into diagnostics mode; Select "D) Exit, Reboot or Disable Diags" again
7. Select "D) Disable Diagnostics" and then "Q) To continue"

Once your Kindle reboots into the normal firmware, it should be jailbroken. At this point you can safely delete the diagnostic_logs folder on the Kindle USB drive.

## GUI Launcher

To manage extensions on your jailbroken Kindle, it's best to use this thing called the GUI Launcher. Here's how to get it:

1. Download [launcher file](http://gr4m.com/NyKFBR)
2. Plug the Kindle to your computer via USB.
3. Copy the file named "update_launcher_1.2.1_install.bin" to your Kindle. Make sure to place it directly in the top-level directory of the USB drive, not in the "documents" subdirectory or in any other subdirectory.
4. Safely eject the Kindle from the computer.
5. On the Kindle, choose Menu -> Settings -> Menu -> Update Your Kindle.

The device will add the GUI Launcher to your Kindle, which you can access by choosing Menu -> Launcher.

## Custom Screensavers

The default screensavers aren't terrible, but the entire purpose of custom screensavers is to make your kindle, yours. To do this you need to run terminal commands on the kindle. The easiest way in my opinion is to use the XTerm extension instead:

1. Download [xterm extension](http://gr4m.com/KFZTih)
2. Extract the extension folder into '/extensions' folder on your Kindle.
3. Safely eject your Kindle, and then restart it (Menu -> Launcher -> Reboot).
4. Launch xterm via: Menu -> Launcher -> Start XTerm
5. In the Xterm prompt, run the following commands (be mindful of the spaces):
  - mntroot rw
  - mkdir /mnt/us/screensavers
  - cp /usr/share/blanket/screensaver/*.png /mnt/us/screensavers/
  - rm -rf /usr/share/blanket/screensaver
  - ln -sfn /mnt/us/screensavers /usr/share/blanket/screensaver
  - exit

Finshed! You'll be able to use any images you like as the screensavers on your Kindle by uploading them in the 'screensavers' folder that will now appear on the Kindle drive. In order for the screensavers to be recognized however, there are some requirements you need to adhere to:

- Screensavers must be PNG images
- They must be 600px by 800px grayscale images.
- All image names must be: 'bg_xsmall_ss##.png' (the ## are two digits starting at 00 and increasing sequentially, i.e. bg_xsmall_ss00.png, bg_xsmall_ss01.png, etc…).

### Octocat Screensavers
The purpose of this repo is to fill your kindle with octocat screensavers. Check the '/screensavers' folder in this for mycollected Octocat images.

## Credits

Again thanks to [@cobyism](https://github.com/cobyism) and [@dreww](https://github.com/dreww) to putting some of these details together and many thanks to the following sites in which many of the instructions and files above were taken from:

- http://wiki.mobileread.com/wiki/Kindle_Touch_Hacking
- http://www.mobileread.com/forums/showthread.php?p=2075539#post2075539
- http://ebookjuggler.com/kindle/removing-ads-on-the-kindle-touch/
- http://www.fabiszewski.net/kindle-xterm/
