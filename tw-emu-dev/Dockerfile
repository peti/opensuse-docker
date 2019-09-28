# Dockerfile for EMU development on openSUSE Tumbleweed.

FROM opensuse/tumbleweed
LABEL maintainer="Peter Simons <simons@cryp.to>"

RUN zypper --non-interactive update     \
 && zypper --non-interactive install -y \
      gcc-c++                           \
      ghostscript                       \
      git                               \
      make                              \
      python                            \
      python3-dateutil                  \
      R                                 \
      rsync                             \
      sqlite3                           \
      texlive-ae                        \
      texlive-fancyvrb                  \
      texlive-isodate                   \
      texlive-parskip                   \
      texlive-substr

RUN Rscript --vanilla -e 'install.packages(c("data.table","xtable","RSQLite","plan"),repos="https://cloud.r-project.org")'

RUN zypper --non-interactive install -y \
      texinfo                           \
      tar

#       openssh                           \
#       osc                               \
#       python-base                       \
#       python-urlgrabber                 \
#       python-xml                        \
#       python2-cssselect                 \
#       python2-lxml                      \
#       python2-M2Crypto                  \
#       python2-pycurl                    \
#       python2-PyYAML                    \
#       python2-rpm                       \
#       python2-typing                    \
