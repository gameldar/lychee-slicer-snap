# Lychee Slicer Snap

This is the source for creating a restricted container for the Lychee Slicer.

It downloads down the `deb` file from the [Lychee Slicer Downloads](https://lychee.mango3d.io/download-lychee-slicer) page and snapcraft unpacks it and adds the required dependencies for it to run.

This is experimental, but appears to be working from the small workflow I need it for.
I've only tested this on Ubuntu 25.04.

## Build & Installation

Assuming you have the [setup snapcraft](https://snapcraft.io/docs/get-started) correctly, to build this snap do the following:
1. Checkout out the repository

```shell
git clone https://github.com/gameldar/lychee-slicer-snap.git
```
2. Run `snapcraft`
3. Install the snap

``` shell
snap install lychee-slicer_7.3.2_amd64.snap --dangerous
```
4. Connected the unconnected plugs. These are not connected by default.

``` shell
snap connect lychee-slicer:userns
snap connect lychee-slicer:steam-support
snap connect lychee-slicer:network-control
```
