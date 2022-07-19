# Installation instructions

## Preparations

Ensure your device has a vendor partition from Android 10 (newer versions only *might* work :( ) Try flashing a Android 10 rom before trying to install.

## Installation

From recovery open adb sideload mode (under advanced on TWRP) and run following commands on your computer replacing `ARCH_YYYYMMDD` with the version of Droidian and `vendor-device` with the vendor and device codenames:

* `adb sideload droidian-rootfs-api28gsi-ARCH_YYYYMMDD.zip`
* `adb sideload droidian-devtools-ARCH_YYYYMMDD.zip`
* `adb sideload droidian-adapatation-vendor-device-ARCH_YYYYMMDD.zip`

Note that you have to restart the sideload mode by tapping back and starting sideload again before every `adb sideload command`.

## Finalizing installation

Now, you have to reboot the device. It should boot to phosh (a graphical user interface used by Droidian) after rebooting once more automatically. When the device has booted, you can unlock the device with the default passcode `1234`.

## Troubleshooting

If the image does not boot and your userdata is not an ext4 partition, you might try formatting it. **Note that this is a destructive operation, you cannot recover files from userdata afterwards!**

* `fastboot format:ext4 userdata`
