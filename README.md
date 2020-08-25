# docker-asuswrt-merlin-build
Asuswrt-Merlin New Gen build environment in the docker.


# Quick Start
- Start a docker container:
```bash
docker run -dt --name asuswrt-merlin-build rex5652/asuswrt-merlin-build
docker exec -it asuswrt-merlin-build bash
```

- Set environment variable for build:
```bash
# For Broadcom SDK6/SDK7 ARM platform (RT-AC56 upto RT-AC5300)
. /root/env/bcm-sdk.sh
# For Broadcom HND ARM platform (RT-AC86U)
#. /root/env/bcm-hnd.sh
# For Broadcom HND AX ARM (RT-AX88U)
#. /root/env/bcm-hnd-802.11ax.sh
```

Then, you can compile your programs, don't forget mount your source code to container.

# Samples
https://gist.github.com/rex5652/31145f85c44dbb8a1f005dd9653fe6b6


cd /tmp
wget https://gist.githubusercontent.com/rex5652/31145f85c44dbb8a1f005dd9653fe6b6/raw/2495dee5cfe520544892adaa7f954f90402e5043/build-shadowsocks-libev-for-asuswrt-merlin.sh

chmod +x build-shadowsocks-libev-for-asuswrt-merlin.sh
./build-shadowsocks-libev-for-asuswrt-merlin.sh

find binary in /home/build/arm/shadowsocks/bin
