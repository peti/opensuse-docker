# Dockerfile for Haskell lts-11.x development on openSUSE Leap.

FROM opensuse/leap
LABEL maintainer="Peter Simons <simons@cryp.to>"

RUN zypper --non-interactive ar -c -p 25 -r https://download.opensuse.org/repositories/devel:/languages:/haskell:/lts:/11/openSUSE_Leap_15.0/devel:languages:haskell:lts:11.repo \
 && zypper --non-interactive --gpg-auto-import-keys refresh \
 && zypper --non-interactive update \
 && zypper --non-interactive install -y \
      alex              \
      bind-utils        \
      cabal-install     \
      doctest           \
      ghc               \
      ghc-weeder        \
      happy             \
      hlint             \
      stack
