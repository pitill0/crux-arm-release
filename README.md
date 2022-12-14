# crux-arm-release
## What is crux-arm-release?
It's the official release builder for CRUX-ARM.

## What can be done with crux-arm-release?
We can take a look to the help command to see what can we do with this repository:
```
make help

Targets:
  help         Show this help information
  stage0       Build stage0 ports compiled against your host
  stage1       Build stage1 ports inside chroot environment
  bootstrap    Build all stages and bootstrap the rootfs
  release      Build CRUX-ARM release

Additional variables to all targets:

  DEVICE_OPTIMIZATION  Device for which we want to optimize the build
                       e.g: make stage1 DEVICE_OPTIMIZATION=odroidxu4
```

## How should I use it as a user?
You only need to use one option (bootstrap) and use the DEVICE_OPTIMIZATION variable
if you are building an optimized release for a specific device.

If you have a not official device, check devices.mk files to create your own
optimization for your specific device

## What do I need to run crux-arm-release?
You need a CRUX host and just two dependencies installed:
- git: needed to get ports collections
- texinfo: needed to build binutils documentation
