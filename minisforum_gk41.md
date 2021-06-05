# BESSTAR / MINISFORUM GK41
Here is a short technical overview for the Minisforum GK41, running Proxmox VE.

# Proxmox on GK41
```
root@pve:~# pveversion
pve-manager/6.4-6/be2fa32c (running kernel: 5.4.114-1-pve)
```

## bios / dmidecode

```
BIOS Information
	Vendor: American Megatrends Inc.
	Version: GB7 0.05
	Release Date: 03/18/2021
	Address: 0xF0000
	Runtime Size: 64 kB
	ROM Size: 4416 kB
	Characteristics:
		PCI is supported
		BIOS is upgradeable
		BIOS shadowing is allowed
		Boot from CD is supported
		Selectable boot is supported
		BIOS ROM is socketed
		EDD is supported
		5.25"/1.2 MB floppy services are supported (int 13h)
		3.5"/720 kB floppy services are supported (int 13h)
		3.5"/2.88 MB floppy services are supported (int 13h)
		Print screen service is supported (int 5h)
		Serial services are supported (int 14h)
		Printer services are supported (int 17h)
		ACPI is supported
		USB legacy is supported
		BIOS boot specification is supported
		Targeted content distribution is supported
		UEFI is supported
	BIOS Revision: 0.5
```

## lscpu

```
Architecture:        x86_64
CPU op-mode(s):      32-bit, 64-bit
Byte Order:          Little Endian
Address sizes:       39 bits physical, 48 bits virtual
CPU(s):              4
On-line CPU(s) list: 0-3
Thread(s) per core:  1
Core(s) per socket:  4
Socket(s):           1
NUMA node(s):        1
Vendor ID:           GenuineIntel
CPU family:          6
Model:               122
Model name:          Intel(R) Celeron(R) J4125 CPU @ 2.00GHz
Stepping:            8
CPU MHz:             537.244
CPU max MHz:         2700.0000
CPU min MHz:         800.0000
BogoMIPS:            3993.60
Virtualization:      VT-x
L1d cache:           24K
L1i cache:           32K
L2 cache:            4096K
NUMA node0 CPU(s):   0-3
Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg cx16 xtpr pdcm sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave rdrand lahf_lm 3dnowprefetch cpuid_fault cat_l2 cdp_l2 ssbd ibrs ibpb stibp ibrs_enhanced tpr_shadow vnmi flexpriority ept vpid ept_ad fsgsbase tsc_adjust smep erms mpx rdt_a rdseed smap clflushopt intel_pt sha_ni xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts umip rdpid md_clear arch_capabilities
```

# lspci

```
00:00.0 Host bridge: Intel Corporation Device 31f0 (rev 06)
00:00.1 Signal processing controller: Intel Corporation Celeron/Pentium Silver Processor Dynamic Platform and Thermal Framework Processor Participant (rev 06)
00:02.0 VGA compatible controller: Intel Corporation Device 3185 (rev 06)
00:0e.0 Multimedia audio controller: Intel Corporation Device 3198 (rev 06)
00:0f.0 Communication controller: Intel Corporation Celeron/Pentium Silver Processor Trusted Execution Engine Interface (rev 06)
00:12.0 SATA controller: Intel Corporation Device 31e3 (rev 06)
00:13.0 PCI bridge: Intel Corporation Device 31d8 (rev f6)
00:13.1 PCI bridge: Intel Corporation Device 31d9 (rev f6)
00:13.2 PCI bridge: Intel Corporation Device 31da (rev f6)
00:14.0 PCI bridge: Intel Corporation Device 31d6 (rev f6)
00:14.1 PCI bridge: Intel Corporation Device 31d7 (rev f6)
00:15.0 USB controller: Intel Corporation Device 31a8 (rev 06)
00:16.0 Signal processing controller: Intel Corporation Celeron/Pentium Silver Processor Serial IO I2C Host Controller (rev 06)
00:16.3 Signal processing controller: Intel Corporation Device 31b2 (rev 06)
00:1c.0 SD Host controller: Intel Corporation Celeron/Pentium Silver Processor SDA Standard Compliant SD Host Controller (rev 06)
00:1f.0 ISA bridge: Intel Corporation Device 31e8 (rev 06)
00:1f.1 SMBus: Intel Corporation Celeron/Pentium Silver Processor Gaussian Mixture Model (rev 06)
01:00.0 Network controller: Qualcomm Atheros QCA9377 802.11ac Wireless Network Adapter (rev 31)
02:00.0 Ethernet controller: Realtek Semiconductor Co., Ltd. RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller (rev 15)
03:00.0 Ethernet controller: Realtek Semiconductor Co., Ltd. RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller (rev 15)
```

