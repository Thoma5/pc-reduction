pc-reduction
============

Scipts to minimize the power consumption of your notebook/pc running on Linux.
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

Warning
-------
Could lead to data loss if your device is not compatible to the techology used (SATA_ALPM,ASPM,...).

Disclaimer
----------
I am not responsible if you use this and brick your device or if you suffer data loss or if your device blows up, implodes, flames start shooting from it or anything else. Use at your own risk. I am not responsible...


