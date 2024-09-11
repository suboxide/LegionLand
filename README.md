! Do not use or try this this will most likely break your system, I use this build to boot my legion go into gamemode, when selecting go to desktop it goes to plasma desktop automaticly. Once there when I click logout I get sddm with options to pick hyprland. (I use this on the go with gamemode and plasma and at home docked hyprland)
 

- First rebase to the unsigned image, to get the proper signing keys and policies installed:
  ```
  rpm-ostree rebase ostree-unverified-registry:ghcr.io/suboxide/legionland:latest
  ```
- Reboot to complete the rebase:
  ```
  systemctl reboot
  ```
- Then rebase to the signed image, like so:
  ```
  rpm-ostree rebase ostree-image-signed:docker://ghcr.io/suboxide/legionland:latest
  ```
- Reboot again to complete the installation
  ```
  systemctl reboot
  ```
