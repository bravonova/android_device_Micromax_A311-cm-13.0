----Thanks to all who are contributing to the working CyanogenMod of MTK hardware.---
# CyanogenMod 13.0

This is a device tree for Micromax Canvas Nitro A311 which is based on MT6592 SoC. Powered by Tirth Patel.
# Build

* init
  Sync CyanogenMod source:

        # repo init -u git://github.com/ferhung-mtk/android.git -b cm-13.0        
        # repo sync

* full build
        
        # source build/envsetup.sh

        # brunch cm_A311-userdebug

# Limitations

Services requires root:

`system/core/rootdir/init.rc`

  * surfaceflinger depends on sched_setscheduler calls, unable to change process priority from 'system' user (default user 'system')

  * mediaserver depends on /data/nvram folder access, unable to do voice calls from 'media' user (default user 'media')

