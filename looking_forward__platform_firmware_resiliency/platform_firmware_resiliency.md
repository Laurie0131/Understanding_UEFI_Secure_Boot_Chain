## Platform Firmware Resiliency {#platform-firmware-resiliency}

In modern platforms, system firmware is only one of multiple firmware images. Most system components rely on some form of device firmware. The scope of PFR covers both system firmware and device firmware images, so the trust chain is maintained for all boot firmware components. See Figure 4-1 for an overview diagram.

![](media/image14.png)

Figure 4-1: Component and Trust Chain, from NIST [SP800-193](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-193.pdf)

Device firmware may exist in a device-specific region that is managed by the device. In some cases, device firmware may reside in the same location as the system firmware, such as Serial Peripheral Interface (SPI) attached to flash, and the system firmware is responsible for loading the device firmware into a device firmware region.

Most device firmware initializes the hardware so it is functional at runtime. Examples include:

*   Network Interface Card (NIC)

*   Solid State Drive (SSD)

*   Universal Serial Bus (USB)

*   Battery management

Some device firmware is involved in the system boot process and may play an important role in system firmware verification. Examples include:

*   Embedded Controller (EC) firmware

*   Baseboard Management Controller (BMC) firmware

*   Intel® Converged Security and Management Engine (Intel® CSME)

*   Glue logic in a Field Programmable Gate Array (FPGA) or Complex Programmable Logic Device (CPLD)

There are multiple existing standards describing device authentication, including:

*   [PCIe Device Security](https://www.intel.com/content/www/us/en/io/pci-express/pcie-device-security-enhancements-spec.html)

*   [USB Authentication](https://www.usb.org/document-library/usb-authentication-specification-rev-10-ecn-and-errata-through-january-7-2019)

*   Security Protocol and Data Model ([SPDM](https://www.dmtf.org/sites/default/files/standards/documents/DSP0274_0.9.0a.pdf))

Figure 4-2 shows a high-level view of an authentication protocol.

![](media/image15.png)

Figure 4-2: High-level View of PCIe® Component Authentication (source: [PCIe® Component Authentication](https://pcisig.com/pcie%C2%AE-component-authentication))