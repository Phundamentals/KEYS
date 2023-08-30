You can get GPG4Win from [here](https://gpg4win.org/)

If you want to install GnuPG without installing any extras (such as Kleopatra):
  - Open the download with 7zip (right mouse click, 7zip > open archive)
  - (Extract $TEMP\gnupg-w32*-bin.exe)
  - Execute gnupg-w32*-bin.exe

Or download only GnuPG from [here](https://www.gnupg.org/ftp/gcrypt/binary/) directly.

You can use the command line option _/D_ to specify an alternate installation path. It should be the last option specified and should NOT be quoted, even if the path contains spaces.
Also note the equals sign. E.g.: _gnupg-w32-2.4.3_20230704.exe /D=C:\GnuPG_
