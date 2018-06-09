# Dockerfile for EMU development on openSUSE Leap.

FROM opensuse/leap
LABEL maintainer="Peter Simons <simons@cryp.to>"

RUN zypper --non-interactive update     \
 && zypper --non-interactive install -y \
      gcc-c++                           \
      ghostscript                       \
      make                              \
      osc                               \
      python                            \
      python-base                       \
      python-urlgrabber                 \
      python-xml                        \
      python2-cssselect                 \
      python2-lxml                      \
      python2-M2Crypto                  \
      python2-pycurl                    \
      python2-PyYAML                    \
      python2-rpm                       \
      python2-typing                    \
      python3-dateutil                  \
      R                                 \
      sqlite3                           \
      tar                               \
      texinfo                           \
      texlive-ae                        \
      texlive-fancyvrb                  \
      texlive-isodate                   \
      texlive-parskip                   \
      texlive-substr

RUN Rscript --vanilla -e 'install.packages(c("data.table","xtable","RSQLite","plan"),repos="https://cloud.r-project.org")'

# RUN zypper --non-interactive ar -c -p 20 -r http://download.suse.de/ibs/NON_Public:/maintenance:/smelt/openSUSE_Leap_15.0/NON_Public:maintenance:smelt.repo \
#  && zypper --non-interactive --gpg-auto-import-keys refresh NON_Public_maintenance_smelt \
#  && zypper --non-interactive install -y smelt \
#  && echo >~/.smelt.conf  '{ "backend": { "database": "/var/lib/smelt" } }'
