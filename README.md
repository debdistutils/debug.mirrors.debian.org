# Git LFS mirror of `debug.mirrors.debian.org`

This git repository contains a mirror of
[debug.mirrors.debian.org](https://debug.mirrors.debian.org/), with
external objects stored using [Git LFS](https://git-lfs.com/).

This repository was created using rsync from [the `ftp.de.debian.org`
mirror of
debug.mirrors.debian.org](https://wiki.debian.org/DebugPackage) on
2024-06-18.  The goal is to keep it in sync with
`debug.mirrors.debian.org` going forward.

## Cloning

The Git LFS objects are not available via GitLab, therefor to clone
this repository successfully you will need to disable Git LFS smudging
using the `GIT_LFS_SKIP_SMUDGE=1` environment variable like this:

```
GIT_LFS_SKIP_SMUDGE=1 git clone https://gitlab.com/debdistutils/archives/debian/debug.mirrors.debian.org.git
```

# Signature Verification

Commits are signed using [my PGP
key](https://blog.josefsson.org/2019/03/21/openpgp-2019-key-transition-statement/)
with fingerprint:

```
pub   ed25519 2019-03-20 [SC]
      B1D2 BD13 75BE CB78 4CF4  F8C4 D73C F638 C53C 06BE
```

Alternatively, the new dedicated importer key with the following
fingerprint:

```
sec   rsa3072 2024-06-15 [SC]
      A6DB 3F7E A841 C2E2 1D5E  72A1 0BC2 D729 80EC B489
uid   Apt archive Git LFS importer <apt2gitlfs@snapt.debian.net>
```

You may view git log and verify commit signatures them as follows:

```
git log --show-signature
```

To verify a single commit use something like this:

```
$ git verify-commit 3f1584b841253b5050d41c7ee49c5b5111a08ffe
gpg: Signature made Tue 18 Jun 2024 10:44:21 PM CEST
gpg:                using RSA key A6DB3F7EA841C2E21D5E72A10BC2D72980ECB489
gpg:                issuer "apt2gitlfs@snapt.debian.net"
gpg: Good signature from "Apt archive Git LFS importer <apt2gitlfs@snapt.debian.net>" [ultimate]
$ 
```

## Contact

The maintainer is [Simon Josefsson](https://blog.josefsson.org/).
