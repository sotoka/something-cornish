# Something Cornish

This firmware intent to replace the ["original" firmware](https://github.com/a741725193/zmk-config-zen-2) that's powering the corne clone found on Aliexpress which is using a 52840nano controller.

The original firmware is a large copy paste of the Corn-ish Zen source code, with some tweak to enable the underglow.

As the main source code for corn-ish zen is now merged into ZMK, it's time for a cleanup.

## How to use :

To create your own configuration use this reposiroty as a ZMK module by adding it in the `west.yml` file and use it in your build file.

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: capmousse
      url-base: https://github.com/CapMousse
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: something-cornish
      remote: capmousse
      revision: main
  self:
    path: config
```

## Features

- [x] Up to date ZMK integration
- [x] Use official template
- [x] Work as a ZMK module
- [x] Custom shield
- [x] Working underglow
- [x] New physical layout support
- [x] ZMK Studio support if enabled
