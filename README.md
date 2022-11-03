# linux-system-confs

My system-wide (/etc/) configuration files. These are generally for Arch
Linux and expect to have my meta-packages installed, though they might
be useful in other setups as well.

This is the general readme for the repo. Top-level directories might
include additional `README.md`s to add package-specific information.

# Installing

The configuration files are managed by GNU `stow`. Each top-level
directory is an independent "package". For example, to install the
pacman configuration files, one would do

    # stow pacman

In many cases the configuration files will already exist, and `stow`
will refuse to overwrite them. One solution is to delete them before
calling `stow`. Alternatively, `--adopt` the files. This will copy
them into this repo so you will have to reset them.

    # stow --adopt pacman
    # git reset --hard
