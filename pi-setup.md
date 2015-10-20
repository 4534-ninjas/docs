# **WE ARE USING COLIN'S MICROSD CARD! MAKE SURE HE GETS IT BACK**

The one they gave us had problems. It would hang on boot with
`mmc0 interrupt timed out` or something like that in the in the dmesg.

## Initial setup

with `raspi-config`:

* Expand Filesystem
* Boot Options -> Console

Added `jpo` user in `sudo` group

Set up SSH keys

Change password for `pi` user

removed MOTD stuff:

* `PrintLastLog no` in `/etc/ssh/sshd_config`
* comment out `pam_motd.so` in `/etc/pam.d/sshd`
* rm `/etc/motd`

Installed packages:

* vim
* zsh
* git
* golang
* silversearcher-ag

See <networking.md> for info about how to set up the wireless dongle.
