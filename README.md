pc-reduction
============

Scipt to minimize the power consumption of your notebook/pc running on Linux.

Currently only tested on my Dell Inspirion Ultrabook (14z 5423).

Requirements
------------

+ A newer linux kernel (>=3.10?)
+ x86_energy_perf_policy installed
+ powertop
+ systemd
+ root for systemctl
+ Intel i* CPU (SandyBridge or newer)
+ setting some kernel parameters (WIFI, ASPM ...)
+ COMPATIBLE NOTEBOOK- Can lead to dataloss on some notebooks (SATA-ALPM, ASPM...)
+ 
Recommended kernel params (additionally to those you already have lieke quiet etc.):
```
acpi_osi='!Windows 2012' acpi_osi='Linux' add_efi_memmap video.use_native_backlight=1 ipv6.disable=1 elevator=noop drm.vblankoffdelay=1 pcie_aspm=force i915.enable_rc6=7 i915.enable_fbc=1 i915.lvds_downclock=1 i915.semaphores=1 nmi_watchdog=0 ath9k.ps_enable=1
```


Warning
-------
Could lead to data loss if your device is not compatible to the techology used (SATA_ALPM,ASPM,...).

Install
-------
To install:
```
git clone https://github.com/Thoma5/pc-reduction.git
cd pc-reduction
sudo cp pc_reduction /usr/lib/systemd/scripts/
sudo cp pc_reduction.service /usr/lib/systemd/system/
sudo chown root:root /usr/lib/systemd/scripts/pc_reduction
sudo chmod +x /usr/lib/systemd/scripts/pc_reduction
sudo chown root:root /usr/lib/systemd/system/pc_reduction.service
```
To activate:
```
sudo systemctl start pc_reduction.service
```
To deactivate:
```
sudo systemctl stop pc_reduction.service
```
For activation on startup:
```
sudo systemctl enable pc_reduction.service
```
and same with disable for deactivating.


Disclaimer
----------
I am not responsible if you use this and brick your device or if you suffer data loss or if your device blows up, implodes, flames start shooting from it or anything else. Use at your own risk. I am not responsible...


