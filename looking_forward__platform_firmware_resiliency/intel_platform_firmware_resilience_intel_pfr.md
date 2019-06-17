## Intel® Platform Firmware Resilience (Intel® PFR) {#intel-platform-firmware-resilience-intel-pfr}

To reduce firmware-related security risks, Intel developed [Intel PFR](https://www.intel.com/content/www/us/en/data-center-blocks/business/firmware-resilience-blocks-solution-brief.html) for server platforms. This feature protects critical firmware from attacks during boot and runtime. It can be treated as an implementation of Project Cerberus or NIST SP800-193.

Intel PFR also enables a protect-in-transit feature, allowing customers to lock and unlock systems to guard against firmware changes during shipment. and “Intel transparent supply chain with platform certificate to create transparency in the supply chain to prevent counterfeit components from being used.”

Figure 4-7 shows the Intel PFR system diagram. Figure 4-8 shows the Intel PFR boot flow. Figure 4-9 shows the Intel PFR reset sequence.

![C:\Users\jyao1\Desktop\back\document\Industry\Intel_CPU_Manual\PFR\Intel Platform Firmware Resilience_files\20181118085448280.PNG](media/image21.png)

Figure 4-7: Intel® PFR Overview (source: [csdn.net](https://blog.csdn.net/zdx19880830/article/details/84190005))

![C:\Users\jyao1\Desktop\back\document\Industry\Intel_CPU_Manual\PFR\Intel Platform Firmware Resilience_files\20181118100107506.PNG](media/image22.png)

Figure 4-8: Intel® PFR boot flow (source: [csdn.net](https://blog.csdn.net/zdx19880830/article/details/84190005))

![C:\Users\jyao1\Desktop\20181118102915674.png](media/image23.png)

Figure 4-9: Intel® PFR Reset Sequence (source: [csdn.net](https://blog.csdn.net/zdx19880830/article/details/84190005))