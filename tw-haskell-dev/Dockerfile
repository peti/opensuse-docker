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

RUN cabal update
