# Refind

Unlike the other packages this cannot be stowed, because the efi partition is
read during early boot and any symlinks it holds to other filesystems will not
be resolveable. Not to mention that vfat doesn't support symbolic links to
begin with. So this package has to be manually copied to the destination.

This package expects refind-theme-regular-git to be installed. refind.conf will
also have to be edited to include the theme file, as normal for installing the
theme.
