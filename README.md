dm1-4160ca
==========

HP Pavilion dm1-4160ca Entertainment Notebook PC (A7G65UA) - kernel configuration

This is a minimal and personal configuration/documentation for this laptop model.

Disclaimer
----------

I'm not an expert in hardware configuration in linux and many of the options was enabled/disabled under a guessing base.

Details
-------

### Kernel

#### uname -a

    Linux maple 3.4.9-gentoo #6 SMP Thu Oct 4 17:28:52 PDT 2012 x86_64 AMD E-450 APU with Radeon(tm) HD Graphics AuthenticAMD GNU/Linux

### Hardware

#### lspci -v

    00:00.0 Host bridge: Advanced Micro Devices [AMD] Family 14h Processor Root Complex
      Subsystem: Advanced Micro Devices [AMD] Family 14h Processor Root Complex
    	Flags: bus master, 66MHz, medium devsel, latency 32
    
    00:01.0 VGA compatible controller: Advanced Micro Devices [AMD] nee ATI Wrestler [Radeon HD 6320] (prog-if 00 [VGA controller])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, fast devsel, latency 0, IRQ 43
    	Memory at e0000000 (32-bit, prefetchable) [size=256M]
    	I/O ports at 4000 [size=256]
    	Memory at f0300000 (32-bit, non-prefetchable) [size=256K]
    	Expansion ROM at <unassigned> [disabled]
    	Capabilities: [50] Power Management version 3
    	Capabilities: [58] Express Root Complex Integrated Endpoint, MSI 00
    	Capabilities: [a0] MSI: Enable+ Count=1/1 Maskable- 64bit+
    	Capabilities: [100] Vendor Specific Information: ID=0001 Rev=1 Len=010 <?>
    	Kernel driver in use: fglrx_pci
    	Kernel modules: fglrx
    
    00:01.1 Audio device: Advanced Micro Devices [AMD] nee ATI Wrestler HDMI Audio [Radeon HD 6250/6310]
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, fast devsel, latency 0, IRQ 42
    	Memory at f0344000 (32-bit, non-prefetchable) [size=16K]
    	Capabilities: [50] Power Management version 3
    	Capabilities: [58] Express Root Complex Integrated Endpoint, MSI 00
    	Capabilities: [a0] MSI: Enable+ Count=1/1 Maskable- 64bit+
    	Capabilities: [100] Vendor Specific Information: ID=0001 Rev=1 Len=010 <?>
    	Kernel driver in use: snd_hda_intel
    
    00:04.0 PCI bridge: Advanced Micro Devices [AMD] Family 14h Processor Root Port (prog-if 00 [Normal decode])
    	Flags: bus master, fast devsel, latency 0
    	Bus: primary=00, secondary=01, subordinate=01, sec-latency=0
    	I/O behind bridge: 00001000-00001fff
    	Memory behind bridge: f0400000-f05fffff
    	Prefetchable memory behind bridge: 00000000f0600000-00000000f07fffff
    	Capabilities: [50] Power Management version 3
    	Capabilities: [58] Express Root Port (Slot+), MSI 00
    	Capabilities: [a0] MSI: Enable+ Count=1/1 Maskable- 64bit+
    	Capabilities: [b0] Subsystem: Advanced Micro Devices [AMD] Device 1234
    	Capabilities: [b8] HyperTransport: MSI Mapping Enable+ Fixed+
    	Capabilities: [100] Vendor Specific Information: ID=0001 Rev=1 Len=010 <?>
    	Kernel driver in use: pcieport
    
    00:11.0 SATA controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 SATA Controller [AHCI mode] (prog-if 01 [AHCI 1.0])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 64, IRQ 19
    	I/O ports at 4118 [size=8]
    	I/O ports at 4124 [size=4]
    	I/O ports at 4110 [size=8]
    	I/O ports at 4120 [size=4]
    	I/O ports at 4100 [size=16]
    	Memory at f034e000 (32-bit, non-prefetchable) [size=1K]
    	Capabilities: [70] SATA HBA v1.0
    	Capabilities: [a4] PCI Advanced Features
    	Kernel driver in use: ahci
    
    00:12.0 USB controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 USB OHCI0 Controller (prog-if 10 [OHCI])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 32, IRQ 18
    	Memory at f034d000 (32-bit, non-prefetchable) [size=4K]
    	Kernel driver in use: ohci_hcd
    
    00:12.2 USB controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 USB EHCI Controller (prog-if 20 [EHCI])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 32, IRQ 17
    	Memory at f034c000 (32-bit, non-prefetchable) [size=256]
    	Capabilities: [c0] Power Management version 2
    	Capabilities: [e4] Debug port: BAR=1 offset=00e0
    	Kernel driver in use: ehci_hcd
    
    00:13.0 USB controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 USB OHCI0 Controller (prog-if 10 [OHCI])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 32, IRQ 18
    	Memory at f034b000 (32-bit, non-prefetchable) [size=4K]
    	Kernel driver in use: ohci_hcd
    
    00:13.2 USB controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 USB EHCI Controller (prog-if 20 [EHCI])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 32, IRQ 17
    	Memory at f034a000 (32-bit, non-prefetchable) [size=256]
    	Capabilities: [c0] Power Management version 2
    	Capabilities: [e4] Debug port: BAR=1 offset=00e0
    	Kernel driver in use: ehci_hcd
    
    00:14.0 SMBus: Advanced Micro Devices [AMD] nee ATI SBx00 SMBus Controller (rev 42)
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: 66MHz, medium devsel
    	Kernel driver in use: piix4_smbus
    
    00:14.2 Audio device: Advanced Micro Devices [AMD] nee ATI SBx00 Azalia (Intel HDA) (rev 40)
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, slow devsel, latency 32, IRQ 16
    	Memory at f0340000 (64-bit, non-prefetchable) [size=16K]
    	Capabilities: [50] Power Management version 2
    	Kernel driver in use: snd_hda_intel
    
    00:14.3 ISA bridge: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 LPC host controller (rev 40)
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 0
    
    00:14.4 PCI bridge: Advanced Micro Devices [AMD] nee ATI SBx00 PCI to PCI Bridge (rev 40) (prog-if 01 [Subtractive decode])
    	Flags: bus master, 66MHz, medium devsel, latency 64
    	Bus: primary=00, secondary=02, subordinate=02, sec-latency=64
    
    00:15.0 PCI bridge: Advanced Micro Devices [AMD] nee ATI SB700/SB800/SB900 PCI to PCI bridge (PCIE port 0) (prog-if 00 [Normal decode])
    	Flags: bus master, fast devsel, latency 0
    	Bus: primary=00, secondary=03, subordinate=06, sec-latency=0
    	I/O behind bridge: 00003000-00003fff
    	Memory behind bridge: f0200000-f02fffff
    	Prefetchable memory behind bridge: 00000000f0000000-00000000f00fffff
    	Capabilities: [50] Power Management version 3
    	Capabilities: [58] Express Root Port (Slot-), MSI 00
    	Capabilities: [a0] MSI: Enable- Count=1/1 Maskable- 64bit+
    	Capabilities: [b0] Subsystem: Advanced Micro Devices [AMD] nee ATI Device 0000
    	Capabilities: [b8] HyperTransport: MSI Mapping Enable+ Fixed+
    	Capabilities: [100] Vendor Specific Information: ID=0001 Rev=1 Len=010 <?>
    	Kernel driver in use: pcieport
    
    00:15.1 PCI bridge: Advanced Micro Devices [AMD] nee ATI SB700/SB800/SB900 PCI to PCI bridge (PCIE port 1) (prog-if 00 [Normal decode])
    	Flags: bus master, fast devsel, latency 0
    	Bus: primary=00, secondary=07, subordinate=07, sec-latency=0
    	I/O behind bridge: 00002000-00002fff
    	Prefetchable memory behind bridge: 00000000f0100000-00000000f01fffff
    	Capabilities: [50] Power Management version 3
    	Capabilities: [58] Express Root Port (Slot-), MSI 00
    	Capabilities: [a0] MSI: Enable- Count=1/1 Maskable- 64bit+
    	Capabilities: [b0] Subsystem: Advanced Micro Devices [AMD] nee ATI Device 0000
    	Capabilities: [b8] HyperTransport: MSI Mapping Enable+ Fixed+
    	Capabilities: [100] Vendor Specific Information: ID=0001 Rev=1 Len=010 <?>
    	Kernel driver in use: pcieport
    
    00:16.0 USB controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 USB OHCI0 Controller (prog-if 10 [OHCI])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 32, IRQ 18
    	Memory at f0349000 (32-bit, non-prefetchable) [size=4K]
    	Kernel driver in use: ohci_hcd
    
    00:16.2 USB controller: Advanced Micro Devices [AMD] nee ATI SB7x0/SB8x0/SB9x0 USB EHCI Controller (prog-if 20 [EHCI])
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, 66MHz, medium devsel, latency 32, IRQ 17
    	Memory at f0348000 (32-bit, non-prefetchable) [size=256]
    	Capabilities: [c0] Power Management version 2
    	Capabilities: [e4] Debug port: BAR=1 offset=00e0
    	Kernel driver in use: ehci_hcd
    
    00:18.0 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 0 (rev 43)
    	Flags: fast devsel
    
    00:18.1 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 1
    	Flags: fast devsel
    
    00:18.2 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 2
    	Flags: fast devsel
    
    00:18.3 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 3
    	Flags: fast devsel
    	Capabilities: [f0] Secure device <?>
    	Kernel driver in use: k10temp
    
    00:18.4 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 4
    	Flags: fast devsel
    
    00:18.5 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 6
    	Flags: fast devsel
    
    00:18.6 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 5
    	Flags: fast devsel
    
    00:18.7 Host bridge: Advanced Micro Devices [AMD] Family 12h/14h Processor Function 7
    	Flags: fast devsel
    
    03:00.0 Network controller: Broadcom Corporation BCM4313 802.11b/g/n Wireless LAN Controller (rev 01)
    	Subsystem: Hewlett-Packard Company Device 1795
    	Flags: bus master, fast devsel, latency 0, IRQ 16
    	Memory at f0200000 (64-bit, non-prefetchable) [size=16K]
    	Capabilities: [40] Power Management version 3
    	Capabilities: [58] Vendor Specific Information: Len=78 <?>
    	Capabilities: [48] MSI: Enable- Count=1/1 Maskable- 64bit+
    	Capabilities: [d0] Express Endpoint, MSI 00
    	Capabilities: [100] Advanced Error Reporting
    	Capabilities: [13c] Virtual Channel
    	Capabilities: [160] Device Serial Number 00-00-85-ff-ff-49-c0-18
    	Capabilities: [16c] Power Budgeting <?>
    	Kernel driver in use: wl
    	Kernel modules: wl
    
    07:00.0 Ethernet controller: Realtek Semiconductor Co., Ltd. RTL8111/8168B PCI Express Gigabit Ethernet controller (rev 06)
    	Subsystem: Hewlett-Packard Company Device 3387
    	Flags: bus master, fast devsel, latency 0, IRQ 41
    	I/O ports at 2000 [size=256]
    	Memory at f0104000 (64-bit, prefetchable) [size=4K]
    	Memory at f0100000 (64-bit, prefetchable) [size=16K]
    	Capabilities: [40] Power Management version 3
    	Capabilities: [50] MSI: Enable+ Count=1/1 Maskable- 64bit+
    	Capabilities: [70] Express Endpoint, MSI 01
    	Capabilities: [b0] MSI-X: Enable- Count=4 Masked-
    	Capabilities: [d0] Vital Product Data
    	Capabilities: [100] Advanced Error Reporting
    	Capabilities: [140] Virtual Channel
    	Capabilities: [160] Device Serial Number 00-00-00-00-00-00-00-00
    	Kernel driver in use: r8169


### Processor

AMD Dual-Core E-450 VISION E2 Technology from AMD - 1.65 GHz

#### cat /proc/cpuinfo

    processor  : 0
    vendor_id	: AuthenticAMD
    cpu family	: 20
    model		: 2
    model name	: AMD E-450 APU with Radeon(tm) HD Graphics
    stepping	: 0
    microcode	: 0x5000101
    cpu MHz		: 1646.486
    cache size	: 512 KB
    physical id	: 0
    siblings	: 2
    core id		: 0
    cpu cores	: 2
    apicid		: 0
    initial apicid	: 0
    fpu		: yes
    fpu_exception	: yes
    cpuid level	: 6
    wp		: yes
    flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl nonstop_tsc extd_apicid aperfmperf pni monitor ssse3 cx16 popcnt lahf_lm cmp_legacy svm extapic cr8_legacy abm sse4a misalignsse 3dnowprefetch ibs skinit wdt arat hw_pstate npt lbrv svm_lock nrip_save pausefilter
    bogomips	: 3292.97
    TLB size	: 1024 4K pages
    clflush size	: 64
    cache_alignment	: 64
    address sizes	: 36 bits physical, 48 bits virtual
    power management: ts ttp tm stc 100mhzsteps hwpstate
    
    processor	: 1
    vendor_id	: AuthenticAMD
    cpu family	: 20
    model		: 2
    model name	: AMD E-450 APU with Radeon(tm) HD Graphics
    stepping	: 0
    microcode	: 0x5000101
    cpu MHz		: 1646.486
    cache size	: 512 KB
    physical id	: 0
    siblings	: 2
    core id		: 1
    cpu cores	: 2
    apicid		: 1
    initial apicid	: 1
    fpu		: yes
    fpu_exception	: yes
    cpuid level	: 6
    wp		: yes
    flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl nonstop_tsc extd_apicid aperfmperf pni monitor ssse3 cx16 popcnt lahf_lm cmp_legacy svm extapic cr8_legacy abm sse4a misalignsse 3dnowprefetch ibs skinit wdt arat hw_pstate npt lbrv svm_lock nrip_save pausefilter
    bogomips	: 3292.97
    TLB size	: 1024 4K pages
    clflush size	: 64
    cache_alignment	: 64
    address sizes	: 36 bits physical, 48 bits virtual
    power management: ts ttp tm stc 100mhzsteps hwpstate


Links
-----

http://h10010.www1.hp.com/wwpc/ca/en/ho/WF06b/321957-321957-3329744-64354-64354-5186797-5218464.html?dnr=1
http://www.bestbuy.ca/en-CA/product/hewlett-packard-hp-pavillion-11-6-laptop-featuring-amd-e-450-dual-core-processor-dm1-4160ca-charcoal-dm1-4160ca/10194440.aspx
http://www.amazon.ca/HP-Pavilion-DM1-4160CA11-6-inch-Notebook-VISION/dp/B00701OUM6
http://cateee.net/lkddb/
http://www.ubuntu.com/certification/catalog/
http://www.kernel-seeds.org/working.html
http://kmuto.jp/debian/hcl/
http://kmuto.jp/debian/hcl/HP/dm1-4160ca