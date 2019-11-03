# docto
Docker engine machine under Yocto OpenEmbedded configuration

This project is meant to create a platform for IOT devices and servers to be:
1. Highly secure - using the yocto project, so minimal unrequired packages are injected
2. Easy customization and deployment - using docker engine, enable easy deployments of workloads on the device

Dependencies (already included as sub-modules):
1. Yocto/Poky (git://git.yoctoproject.org/poky)
2. Meta-virtualization (git://git.yoctoproject.org/meta-virtualization)
3. Meta-openembedded (git://git.openembedded.org/meta-openembedded)
4. Meta-intel -optional - for intel support (http://git.yoctoproject.org/git/meta-intel)

Make sure to check those dependencies licenses!

To build the image:
-------------------
1. Use git to clone
2. Use git featch sub-modules
3. cd docto
4. source poky/oe-init-build-env
5. update the necessery destination machine under the file build/conf/local.conf
6. bitbake core-image-base

To run it under qemu:
---------------------
runqemu nographic

Or if it was built for another machine the image should be inside build/tmp/deploy/images

Current status:
---------------
Stable and working
