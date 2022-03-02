# how-to-fix-gpg

      Get:1 http://security.debian.org/debian-security buster/updates InRelease [65.4 kB]
      Get:2 http://deb.debian.org/debian buster InRelease [122 kB]
      Get:3 http://deb.debian.org/debian buster-updates InRelease [51.9 kB]
      Err:1 http://security.debian.org/debian-security buster/updates InRelease
        The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 112695A0E562B32A NO_PUBKEY 54404762BBB6E853
      Err:2 http://deb.debian.org/debian buster InRelease
        The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 648ACFD622F3D138 NO_PUBKEY 0E98404D386FA1D9 NO_PUBKEY DCC9EFBF77E11517
      Err:3 http://deb.debian.org/debian buster-updates InRelease
        The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 648ACFD622F3D138 NO_PUBKEY 0E98404D386FA1D9
      Hit:4 http://repo.zevenet.com/ce/v5 buster InRelease
      Reading package lists... Done
      W: GPG error: http://security.debian.org/debian-security buster/updates InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 112695A0E562B32A NO_PUBKEY 54404762BBB6E853
      E: The repository 'http://security.debian.org/debian-security buster/updates InRelease' is not signed.
      N: Updating from such a repository can't be done securely, and is therefore disabled by default.
      N: See apt-secure(8) manpage for repository creation and user configuration details.
      W: GPG error: http://deb.debian.org/debian buster InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 648ACFD622F3D138 NO_PUBKEY 0E98404D386FA1D9 NO_PUBKEY DCC9EFBF77E11517
      E: The repository 'http://deb.debian.org/debian buster InRelease' is not signed.
      N: Updating from such a repository can't be done securely, and is therefore disabled by default.
      N: See apt-secure(8) manpage for repository creation and user configuration details.
      W: GPG error: http://deb.debian.org/debian buster-updates InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 648ACFD622F3D138 NO_PUBKEY 0E98404D386FA1D9
      E: The repository 'http://deb.debian.org/debian buster-updates InRelease' is not signed.
      N: Updating from such a repository can't be done securely, and is therefore disabled by default.
      N: See apt-secure(8) manpage for repository creation and user configuration details.
root@sv-zevenet-01:~# sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 112695A0E562B32A
-bash: sudo: command not found
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 112695A0E562B32A
Executing: /tmp/apt-key-gpghome.HLmHMFs9xI/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 112695A0E562B32A
gpg: key 4DFAB270CAA96DFA: 5 signatures not checked due to missing keys
gpg: key 4DFAB270CAA96DFA: public key "Debian Security Archive Automatic Signing Key (10/buster) <ftpmaster@debian.org>" imported
gpg: Total number processed: 1
gpg:               imported: 1
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 54404762BBB6E853
Executing: /tmp/apt-key-gpghome.YzwOHtSw8n/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 54404762BBB6E853
gpg: key A48449044AAD5C5D: 4 signatures not checked due to missing keys
gpg: key A48449044AAD5C5D: public key "Debian Security Archive Automatic Signing Key (11/bullseye) <ftpmaster@debian.org>" imported
gpg: Total number processed: 1
gpg:               imported: 1
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 648ACFD622F3D138
Executing: /tmp/apt-key-gpghome.VL6dFiOCBf/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 648ACFD622F3D138
gpg: key DC30D7C23CBBABEE: 4 signatures not checked due to missing keys
gpg: key DC30D7C23CBBABEE: public key "Debian Archive Automatic Signing Key (10/buster) <ftpmaster@debian.org>" imported
gpg: Total number processed: 1
gpg:               imported: 1
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9
Executing: /tmp/apt-key-gpghome.WeVoW7uvaw/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9
gpg: key 73A4F27B8DD47936: 3 signatures not checked due to missing keys
gpg: key 73A4F27B8DD47936: public key "Debian Archive Automatic Signing Key (11/bullseye) <ftpmaster@debian.org>" imported
gpg: Total number processed: 1
gpg:               imported: 1
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys DCC9EFBF77E11517
Executing: /tmp/apt-key-gpghome.Z4LTsaivzc/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys DCC9EFBF77E11517
gpg: key DCC9EFBF77E11517: 3 signatures not checked due to missing keys
gpg: key DCC9EFBF77E11517: public key "Debian Stable Release Key (10/buster) <debian-release@lists.debian.org>" imported
gpg: Total number processed: 1
gpg:               imported: 1
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 648ACFD622F3D138
Executing: /tmp/apt-key-gpghome.NM8Uvg6RYY/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 648ACFD622F3D138
gpg: key DC30D7C23CBBABEE: 4 signatures not checked due to missing keys
gpg: key DC30D7C23CBBABEE: "Debian Archive Automatic Signing Key (10/buster) <ftpmaster@debian.org>" not changed
gpg: Total number processed: 1
gpg:              unchanged: 1
root@sv-zevenet-01:~# apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9
Executing: /tmp/apt-key-gpghome.tzWIuNaL4u/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9
gpg: key 73A4F27B8DD47936: 3 signatures not checked due to missing keys
gpg: key 73A4F27B8DD47936: "Debian Archive Automatic Signing Key (11/bullseye) <ftpmaster@debian.org>" not changed
gpg: Total number processed: 1
gpg:              unchanged: 1
