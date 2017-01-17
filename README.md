## TWRP device tree for OnePlus 3T (oneplus3t)

Add to `.repo/local_manifests/oneplus3t.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/oneplus/oneplus3t" name="android_device_oneplus_oneplus3t" remote="TeamWin" revision="android-6.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_oneplus3t-eng
make -j5 recoveryimage
```

If you want to use the f2fs backport kernel, use `make -j5 USE_F2FS_BACKPORT=1 recoveryimage` instead.  

Kernel sources are available at: https://github.com/jcadduono/android_kernel_oneplus_msm8996/tree/3T-twrp-6.0
