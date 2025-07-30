- https://wiki.archlinux.org/title/Power_management/Suspend_and_hibernate#Hibernation
- https://wiki.archlinux.org/title/Mkinitcpio#Image_creation_and_activation
- https://wiki.archlinux.org/title/Swap


## FAQ

### Computer will not hibernate while using Gnome

This can show up as many things:
- Gnome won't let change what the power button does.
- When the power button is set to hibernate, it will instead go for power off while applications having some action in progress

You can use `gnome-session-inhibit --list` to see what is inhibiting it from hibernating/suspend in Gnome. Generally this tells you what program to close to be able to hibernate.
