# Buildroot study

Buildroot is a simple, efficient and easy-to-use tool to generate embedded
Linux systems through cross-compilation.

## Download

Download the program for your platform from the latest [build action](link).

## Build & usefull commands

```sh
sudo apt install sed make binutils build-essential diffutils gcc g++ bash patch gzip bzip2 perl tar cpio unzip rsync file bc findutils wget libncurses5-dev
git clone https://github.com/buildroot/buildroot
cd buildroot
make list-defconfigs | grep "raspberrypi"
make raspberrypi3_defconfig
make menuconfig # if you want to configure stuff
make
cat output/build/build-time.log # to check the build time
```

### Dependencies

- [buildroot](https://buildroot.org)
- LVGL

## Links

- official manual: https://buildroot.org/downloads/manual/manual.html
- raspi conf: https://rickcarlino.com/2021/building-tiny-raspberry-pi-linux-images-with-buildroot.html
- LVGL: https://blog.lvgl.io/2018-01-03/linux_fb
- build speed: https://www.nayab.dev/linux/build/buildroot/tips/speed-up-buildroot-build

## License

This software is open source and released under [this License](./LICENSE.txt).
