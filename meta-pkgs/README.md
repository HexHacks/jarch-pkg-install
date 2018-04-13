
# Packages

## jarch-base
The minimum system for jarch (Jacob Arch Linux).

# Creating new pkgs

A meta package cannot depend on other Arch meta packages. That means that we have to expand them before putting them in our depends-section.

To expand an existing Arch meta package:
'''
> pacman -Sqg base
bash \
bzip2 \
coreutils \
... \
which \
xfsprogs
'''

This gets put in the depends section of PKGBUILD:
> depends=( \
>&nbsp;&nbsp;&nbsp;&nbsp;'bash' \
>&nbsp;&nbsp;&nbsp;&nbsp;'bzip2' \
>&nbsp;&nbsp;&nbsp;&nbsp;'coreutils' \
>&nbsp;&nbsp;&nbsp;&nbsp;... \
>&nbsp;&nbsp;&nbsp;&nbsp;'which' \
>&nbsp;&nbsp;&nbsp;&nbsp;'xfsprogs' \
> )
