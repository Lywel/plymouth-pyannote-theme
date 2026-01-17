# Plymouth Pyannote Theme

A Plymouth boot splash theme with Pyannote logo and animation for Arch Linux.

## Installation on Arch Linux

### Prerequisites

1. **Add Plymouth hook to mkinitcpio**:

   Edit `/etc/mkinitcpio.conf` and find the `HOOKS=` line and add `plymouth` after `base` and `systemd` (`udev` instead if not using systemd):
   ```
   HOOKS=(base systemd plymouth ...)
   ```

2. **Add quiet splash to kernel parameters**:

   Edit your bootloader configuration:

   - **For GRUB**: Edit `/etc/default/grub` at `GRUB_CMDLINE_LINUX_DEFAULT`:
     ```
     GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
     ```
     Regenerate GRUB config:
     ```bash
     sudo grub-mkconfig -o /boot/grub/grub.cfg
     ```

   - **For systemd-boot**: Edit `/boot/loader/entries/*.conf` append `quiet splash` to the options line.

   - **For UKI**: Edit `/etc/kernel/cmdline` append `quiet splash`.

### Install This Theme

1. Clone or download this repository
2. Build and install the package:
   ```bash
   makepkg -si
   ```

The theme will be automatically set as default and the initrd will be rebuilt.

3. **Reboot** to see your new Plymouth boot splash!

## Change Theme (Optional)

To switch to a different theme later:
```bash
sudo plymouth-set-default-theme -R <theme-name>
```

List available themes:
```bash
plymouth-set-default-theme -l
```
