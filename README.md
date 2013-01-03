Arch Linux Package : systemd-git
================================

Package URL : none
-----------

Related Packages
----------------

  * https://aur.archlinux.org/packages/systemd-git
  * https://www.archlinux.org/packages/core/x86_64/systemd

Notes
-----

This is the AUR systemd-git package modified to include my patch to provide a solution to 
the inability of systemd to generate units for overmounts defined in `/etc/fstab`.

My changes:

  * supply a new patch file called `fstab-overmount.patch`.
  * modify to the `PKGBUILD` to apply the patch.

This package was produced and tested on Thursday 3rd January 2013 to support submission
of a patch to the systemd developers. It is not uploaded to the AUR because I don't 
maintain the systemd-git package.

###Build

    $ git clone https://github.com/johnlane/archlinux-systemd systemd-git
    $ cd systemd-git
    $ makepkg -s

###Install

    $ sudo pacman -U *pkg.tar.xz
