# Public keys and configuration files for GnuPG, SSH, and Git

GPG and SSH commit signing keys, scripts, and configuration. Only the public part of the keys is listed here, of course.
Both the SSH (past) and GPG (present) keys are used for signing. You can use these to verify my signatures, if neccessary.

This setup must be tweaked/adapted to your environment, and is not really plug and play.
It just _might_ help you setup authentication over SSH plus commit signing with only GPG keys.

Most of this is geared towards Windows, but I suppose Linux users should not have many problems adapting it :trollface:,
since GPG, SSH, and Git cooperate almost flawlessly on that OS. I got it to work without problems.

Main goals:
  - Use a single mechanism for authentication and signing (GPG), with the option to make PIN and password caching uniform.
  - Use GPG for Git commit signing, since SSH commit signing does not work well or does not work at all on some SSH versions.
  - Use the very same mechanism (and keys) for signing and encrypting arbitrary data.
  - Prepare for storing these keys on a [YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP).
  - Learn more about GPG / GnuPG.

Note that some of this stuff is Windows only, and some is Linux only. Please read the comments and apply your instincts.

If GPG commands don't working correctly when run from Git Bash on Windows, then try Git Cmd.

See also:
  - https://wiki.debian.org/Subkeys
  - https://github.com/drduh/config/blob/master/gpg.conf
  - https://www.gnupg.org/documentation/manuals/gnupg/GPG-Configuration-Options.html
  - https://www.gnupg.org/documentation/manuals/gnupg/GPG-Esoteric-Options.html
  - https://gist.github.com/mcattarinussi/834fc4b641ff4572018d0c665e5a94d3

For SSH signing, which does work with Git and GitHub out of the box, but might conflict with your SSH version:
  - https://gist.github.com/Phundamentals/68f212191330e857c6b0a34d53db90a2
  - https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows

Software:
  - https://github.com/PowerShell/Win32-OpenSSH/releases
  - https://www.putty.org/
  - https://gpg4win.org/
  - https://git-scm.com/

Yubico software:
  - https://www.yubico.com/support/download/yubikey-manager/
  - https://www.yubico.com/products/yubico-authenticator/
  - https://www.yubico.com/support/download/smart-card-drivers-tools/

A personal recommendation for an SSH client on Windows that:
  - Enables you to to use SSH plus offers a graphical SFTP client.
  - Enables you to have _multiple_ windows/sessions open over a _single_ authentication channel without reauthenticating.
  - Sits as an icon on your task bar letting you open and close new terminals with ease.
  - Holds the connection open as long as the icon is in the taskbar, and tries to reconnect if neccessary.
  - Never gives me problems with keyboard configurations.
  - Is free for personal and commercial use.

  https://www.bitvise.com/ssh-client
