# how-to-fix-gpg

      Get:1 http://security.debian.org/debian-security buster/updates InRelease [65.4 kB]
      Get:2 http://deb.debian.org/debian buster InRelease [122 kB]
      Get:3 http://deb.debian.org/debian buster-updates InRelease [51.9 kB]
      Err:1 http://security.debian.org/debian-security buster/updates InRelease
        The following signatures couldn't be verified because the public key is not available: NO_PUBKEY **112695A0E562B32A** NO_PUBKEY 54404762BBB6E853
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


# Advertise the key from error message above **112695A0E562B32A**
for example 

      apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 112695A0E562B32A

      Executing: /tmp/apt-key-gpghome.HLmHMFs9xI/gpg.1.sh --keyserver keyserver.ubuntu.com --recv-keys 112695A0E562B32A
      gpg: key 4DFAB270CAA96DFA: 5 signatures not checked due to missing keys
      gpg: key 4DFAB270CAA96DFA: public key "Debian Security Archive Automatic Signing Key (10/buster) <ftpmaster@debian.org>" imported
      gpg: Total number processed: 1
      gpg:               imported: 1


