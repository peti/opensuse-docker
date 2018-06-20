# Dockerfile for Haskell development on openSUSE Tumbleweed.

FROM opensuse/tumbleweed
LABEL maintainer="Peter Simons <simons@cryp.to>"

RUN zypper --non-interactive install -y \
      alex                              \
      bind-utils                        \
      cabal-install                     \
      ghc                               \
      happy                             \
      stack

# Create build user (with sudo access).

RUN zypper --non-interactive install -y sudo \
 && sed -i -e "s/^# %wheel ALL=(ALL) NOPASSWD: ALL/%root ALL=(ALL) NOPASSWD: ALL/" /etc/sudoers \
 && useradd -c "Build User" -u 1000 -g users -G root -m -s /bin/bash build
USER build
WORKDIR /home/build
