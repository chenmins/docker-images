# Introduction
This folder contains the information and examples of how to use [Tuxedo TMA](http://docs.oracle.com/cd/E72452_01/tuxedo/docs1222/interm/mainfrm.html) with [Docker](https://www.docker.com/).

## Contents
It is based on the Oracle Tuxedo ART image.

## To use
Pre-installation
Please refer to the README in the root directory to apply rolling patch for Tuxedo.
Download all installers required from [OTN](http://www.oracle.com/technetwork/middleware/tuxedo/downloads/index.html).
1. Tuxedo TMA SNA 12.2.2 Linux 64 bit installer
     tmasna122200_64_linux_x86_64.zip
2. Tuxedo TMA TCP 12.2.2 Linux 64 bit installer
     tmatcp122200_64_linux_x86_64.zip

Installation:
docker build -t oracle/tuxedoartrttma:12.2.2.1 .

You can then start the image in a new container with: ``docker run -d -v \${LOCAL_DIR}:/u01/oracle/user_projects oracle/tuxedoartrttma:12.2.2.1``.
Note: \${LOCAL_DIR} is a local dir which used in docker image as external storage, it can be any dir.
