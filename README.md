# Setup

## Sudoers

```
user ALL=(ALL) NOPASSWD: /usr/bin/systemctl stop docker, /usr/bin/systemctl stop docker.socket, /usr/bin/systemctl stop containerd, /usr/bin/systemctl start docker, /usr/bin/systemctl start docker.socket, /usr/bin/ip link delete *
```

## Flatpak
```
flatpak override --user --filesystem=xdg-config/gtk-3.0
flatpak override --user --filesystem=xdg-config/gtk-4.0
```
## GNOME Dash to Dock bindings

```
#!/bin/bash
for i in 1 2 3 4 5 6 7 8 9; do
  gsettings set org.gnome.shell.keybindings switch-to-application-$i "[]"
done
```
```
dconf write /org/gnome/shell/extensions/dash-to-dock/hot-keys false sleep 1 dconf write /org/gnome/shell/extensions/dash-to-dock/hot-keys true
```
