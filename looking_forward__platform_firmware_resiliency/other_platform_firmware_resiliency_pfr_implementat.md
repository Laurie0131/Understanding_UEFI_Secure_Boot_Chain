## Other Platform Firmware Resiliency (PFR) Implementations {#other-platform-firmware-resiliency-pfr-implementations}

Additional PFR solutions are available for implementing NIST SP800-193, such as the [Lattice Root of Trust FPGA solution](http://www.latticesemi.com/pfr) (see Figure 4-12).

![C:\Users\jyao1\Desktop\back\document\Industry\Intel_CPU_Manual\PFR\otherPFR\PRF_BD.png](media/image26.png)

Figure 4-12: Lattice PFR (source: [latticesemi.com/pfr](http://www.latticesemi.com/pfr)).

The difference in implementations is hardware RoT device selection. Selections include processor microcode, CPLD devices, or FPGA devices. Each has its particular advantages and disadvantages. For example, processor microcode has a limited protection scope, which is why many customers use add-on devices for hardware RoT (CPLD, FPGA).