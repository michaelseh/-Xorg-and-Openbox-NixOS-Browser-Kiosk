# -Xorg-and-Openbox-NixOS-Browser-Kiosk
[Xorg and Openbox] NixOS Browser Kiosk<br><br>
![screenshot]([stripped-Screenshot 2025-04-18 at 18-17-17 DuckDuckGo - Protection. Privacy. Peace of mind.png](https://raw.githubusercontent.com/michaelseh/-Xorg-and-Openbox-NixOS-Browser-Kiosk/refs/heads/main/stripped-Screenshot%202025-04-18%20at%2018-17-17%20DuckDuckGo%20-%20Protection.%20Privacy.%20Peace%20of%20mind.png))

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
