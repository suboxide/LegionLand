!!! Do not use or try this this will most likely break your system !!! 

I use this build to boot my legion go into gamemode, when selecting go to desktop it goes to my custom SDDM 
for this I use a custom sddm theme since it needs to be easy with touch.
I also have a systemd executed that on boot overwrites /ets/sddmconfd/zz. ... to set in the on boot gamemode so it boots to there
I use /usr/local/share/... to set my sddm theme and also the folders set in sddm.conf for wayland and x11.
Probably missing a bunch of things but this is just me making my own stuff so I can use bazzite and test window managers.

  ```
  rpm-ostree rebase ostree-unverified-registry:ghcr.io/suboxide/legionland:latest
  systemctl reboot
  rpm-ostree rebase ostree-image-signed:docker://ghcr.io/suboxide/legionland:latest
  systemctl reboot
  ```
