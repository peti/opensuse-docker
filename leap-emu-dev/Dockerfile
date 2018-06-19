# Dockerfile for EMU development on openSUSE Leap.

FROM opensuse/leap
LABEL maintainer="Peter Simons <simons@cryp.to>"

RUN zypper --non-interactive update     \
 && zypper --non-interactive install -y \
      gcc-c++                           \
      ghostscript                       \
      git                               \
      make                              \
      openssh                           \
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
      rsync                             \
      sqlite3                           \
      tar                               \
      texinfo                           \
      texlive-ae                        \
      texlive-fancyvrb                  \
      texlive-isodate                   \
      texlive-parskip                   \
      texlive-substr

RUN Rscript --vanilla -e 'install.packages(c("data.table","xtable","RSQLite","plan"),repos="https://cloud.r-project.org")'

# build@a86b9d6102f2:~> Rscript -e 'dir.create(Sys.getenv("R_LIBS_USER"), recursive=T)'
# build@a86b9d6102f2:~> Rscript --vanilla -e 'install.packages(c("xtable"),lib=Sys.getenv("R_LIBS_USER"),repos="https://cloud.r-project.org")'
