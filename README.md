# Buildroot study

[![build](https://github.com/314rs/buildroot_study/actions/workflows/build.yaml/badge.svg)](https://github.com/314rs/buildroot_study/actions/workflows/build.yaml)

Build an embedded linux image using buildroot

## Download

Download the program for your platform from the latest [build action](https://github.com/314rs/buildroot_study/actions/workflows/build.yaml).

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
the image then is at `buildroot/output/images/sdcard.img`.

### Dependencies

- [buildroot](https://buildroot.org)
- [LVGL](https://lvgl.io/)

## Links

- official manual: https://buildroot.org/downloads/manual/manual.html
- raspi conf: https://rickcarlino.com/2021/building-tiny-raspberry-pi-linux-images-with-buildroot.html
- LVGL: https://blog.lvgl.io/2018-01-03/linux_fb
- build speed: https://www.nayab.dev/linux/build/buildroot/tips/speed-up-buildroot-build

## License

This software is open source and released under [this License](./LICENSE.txt).
