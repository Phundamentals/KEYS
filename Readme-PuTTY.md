PuTTY's plink is needed to bridge the gap between Git and gpg-agent:
Git's implementation of SSH cannot communicatie with GPG agent.
OpenSSH-Win didn't work in my case, either.

Most of this has to do with *nix using domain sockets and Windows using pipes for inter-process communication.
The software has been ported to Windows, and disagree on how to implement sockets.
Git SSH(-agent)'s implementation on Windows is incompatible with the other software used here, such as GnuPG.

You can configure the SSH command Git uses in the _.gitconfig_ file.
