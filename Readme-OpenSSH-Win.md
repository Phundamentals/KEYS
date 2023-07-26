Git's SSH and gpg-agent don't play well together on Windows. Their socket implementations are very different,
and as such, they are unable to communicate. That's why we use PuTTY and put it before Git on the path.
You can install and test OpenSSH-Win as well, if you want to. It did'nt work for me.

You can download and extract OpenSSH-Win64.zip to a directory without installing it, so it doesn't mess with
other SSH installations.

_Note that this is not actually neccessary for Git to communicate over SSH, since we use PuTTY's plink for that._
