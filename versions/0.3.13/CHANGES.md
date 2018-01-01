Notes:

- The RELEASES is the latest stable version,
- The pre-release is the latest development version,

Files:

- system.zip - archive with individual partitions to be used with rkflashkit,
- system-update.zip - archived update.img to be used with AndroidTool or upgrade_tool,
- system-raw.img.gz - compressed disk image to be used with Etcher, for SD or eMMC,

# 0.3.x

- 0.3.13: Greatly improve Rockbox performance by reducing memory pressure and configuring built-in low memory mode,
- 0.3.13: Allocate full-hd FB instead of 4K one, it frees about 80MB of RAM,
- 0.3.12: Update kernel, device/rockchip/common, packages/app/TvSettings, vendor/rockchip/common to latest changeset: 170930,
- 0.3.12: Build images for Rockbox,
- 0.3.11: Finally fix suspend/resume... :)
- 0.3.10: Make regular to be engineering build for now,
- 0.3.9: Fix booting after changing to 2GB system,
- 0.3.8: Make system to be 2GB,
- 0.3.8: Fix suspend/resume,
- 0.3.8: Pre-dex the build: speed-up the initial boot,
- 0.3.7: DO NOT USE: Test release to check Regular build,
- 0.3.6: Add support for a lot of audio codecs (port of CM soft ffmpeg): https://github.com/ayufan-rock64/android_external_stagefright-plugins/blob/cm-14.1/data/media_codecs_ffmpeg.xml#L21,
- 0.3.5: Properly advertise AVC/High/Level51,
- 0.3.5: Do not show USB connected when booting from SD, instead present eMMC as "external drive then",
- 0.3.4: Make setup wizard to be completed: thus make Home work on IR Remote,
- 0.3.3: Add fix_performance.sh script to improve IRQ mapping: CPU0 (rest), CPU1 (USB2/MMC), CPU2 (USB3), CPU3 (ethernet)
- 0.3.1: Use rk3328_ddr_333MHz_v1.08 and rk322xh_miniloader_v2.44,
- 0.3.0: Include bunch of patches from Rockchip/Pine Inc that should improve 4K playback,

