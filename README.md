# (Xorg and Openbox) NixOS Browser Kiosk
![screenshot](Firefox-Kiosk-Example.png)

## Needs
- Computer with NixOS installation
- Firefox
- Xorg
- Openbox

## How To
- Save xorg.nix file to the following path __/etc/nixos__
- Save hardware-configuration.nix to the following path __/etc/nixos__
  * (make new file depending on your system's hardware)
- Save configuration.nix to the following path __/etc/nixos__
  * (my config w/ Nvidia Drivers, you may not need)

- Import the xorg and hardware configuration in __/etc/nixos/configuration.nix__

## Rebuild
$ sudo nixos-rebuild switch

## Additional Notes
- You can prevent the user from escaping the kiosk into Openbox WM, by using Firefox's __about:config__ settings.
  * Look up browser.tabs.closeWindowWithLastTab and set it to __false__
  * Look up browser.quitShortcut.disabled and set it to __true__

Many thanks to stigok's [blog post](https://blog.stigok.com/2020/06/20/nixos-xserver-openbox-auto-start-browser-application.html) which was the basis of this install!
