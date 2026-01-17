# Plymouth Pyannote Theme

A Plymouth boot splash theme with Pyannote logo and animation for Arch Linux.

## Local Installation

1. Clone or download this repository
2. Build and install the package:
   ```bash
   makepkg -si
   ```

The theme will be automatically set as default and the initrd will be rebuilt. Reboot to see the new boot splash.

## Change Theme (Optional)

To switch to a different theme later:
```bash
sudo plymouth-set-default-theme -R <theme-name>
```

List available themes:
```bash
plymouth-set-default-theme -l
```
