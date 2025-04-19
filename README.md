# -Xorg-and-Openbox-NixOS-Browser-Kiosk
[Xorg and Openbox] NixOS Browser Kiosk
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

## Needs
- Computer with NixOS installation
- Firefox
- Xorg
- Openbox

## How To
- Save xorg.nix file to the following path __/etc/nixos__
- Save hardware-configuration.nix to the following path __/etc/nixos__ (different depending on your system's hardware)
- Save configuration.nix to the following path __/etc/nixos__

- Import the xorg and hardware configuration in __/etc/nixos/configuration.nix__

## Rebuild
$ sudo nixos-rebuild switch

## Additional Notes
- You can prevent the user from escaping the kiosk into Openbox, by using Firefox's about:config settings.
  * Look up browser.tabs.closeWindowWithLastTab and set it to __false__
  * Look up browser.quitShortcut.disabled to __true__

Many thanks to stigok's [blog post](https://blog.stigok.com/2020/06/20/nixos-xserver-openbox-auto-start-browser-application.html) which was the basis of this install!
