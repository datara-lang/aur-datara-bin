# datara-bin (Arch Linux AUR)

Official Arch User Repository (AUR) package source for Datara and the Forgen compiler.

## Installation

### Using an AUR helper (yay / paru)
```bash
yay -S datara-bin
# or
paru -S datara-bin
```

### Manual installation via makepkg
```bash
git clone https://github.com/datara-lang/aur-datara-bin.git
cd aur-datara-bin
makepkg -si
```

## Verification
```bash
forgen --version
datara --version
```
