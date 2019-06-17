## Project Cerberus {#project-cerberus}

As part of the Open Compute Project (OCP), Project Cerberus defines a hierarchical Root of Trust (RoT) architecture. All active components are required to support both hardware and firmware combined identifing through the Device Identifier Composition Engine (DICE).

Figure 4-3 thru 4-6 describe the power on sequence, boot flow, recovery flow, and firmware update flow.

![](media/image16.png)

Figure 4-3: Cerberus power on sequence (source: “[Project Cerberus Hardware Security](https://f990335bdbb4aebc3131-b23f11c2c6da826ceb51b46551bfafdc.ssl.cf2.rackcdn.com/images/fbbdd5feceb6e6328373417e1ab7c06a13a2ef2c.pdf)”)

![](media/image17.png)

Figure 4-4: Cerberus boot flow (source: “[Project Cerberus Hardware Security](https://f990335bdbb4aebc3131-b23f11c2c6da826ceb51b46551bfafdc.ssl.cf2.rackcdn.com/images/fbbdd5feceb6e6328373417e1ab7c06a13a2ef2c.pdf)”)

![](media/image18.png)

Figure 4-5: Cerberus recovery flow (source: “[Project Cerberus Hardware Security](https://f990335bdbb4aebc3131-b23f11c2c6da826ceb51b46551bfafdc.ssl.cf2.rackcdn.com/images/fbbdd5feceb6e6328373417e1ab7c06a13a2ef2c.pdf)”)

![](media/image19.png)![](media/image20.png)

Figure 4-6: Cerberus firmware update (source: “[Project Cerberus Hardware Security](https://f990335bdbb4aebc3131-b23f11c2c6da826ceb51b46551bfafdc.ssl.cf2.rackcdn.com/images/fbbdd5feceb6e6328373417e1ab7c06a13a2ef2c.pdf)”)

The concept of Cerberus is similar to Intel® Boot Guard., but there are several key differences:

1.  Intel® Boot Guard uses Microcode as RoT, while Cerberus uses a dedicated RoT device.

2.  Intel® Boot Guard can mitigate hardware bus attacks.

3.  Intel® Boot Guard only verifies the host system firmware, while Cerberus verifies all boot firmware (platform firmware, BMC, etc.)

4.  Cerberus defines a detailed flow for update and recovery.

Table 4-3: Cerberus Boot

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Boot Firmware Verification (in Cerberus Microcontroller) | OEM | Flash (Read Only Code), Device ROM. |
| **CDI** | Cerberus Microcontroller | OEM | Flash (Read Only Code), Device ROM. |
|  | Boot Firmware Signature Database (Policy) | OEM | Flash (Read Only Data), ROM |
| **UDI** | Boot Firmware (BMC, Firmware) | OEM/IHV | Flash (Read Only Data) – active area |

Table 4-4: Cerberus Recovery

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Boot Firmware Verification (in Cerberus Microcontroller) | OEM | Flash (Read Only Code), Device ROM. |
| **CDI** | Cerberus Microcontroller | OEM | Flash (Read Only Code), Device ROM. |
|  | Boot Firmware Signature Database (Policy) | OEM | Flash (Read Only Data), ROM |
| **UDI** | Boot Firmware Recovery (BMC, Firmware) | OEM/IHV | Flash (Read Only Data) - recovery area |

Table 4-5: Cerberus Firmware Update

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Boot Firmware Verification (in Cerberus Microcontroller) | OEM | Flash (Read Only Code), Device ROM. |
| **CDI** | Cerberus Microcontroller | OEM | Flash (Read Only Code), Device ROM. |
|  | Boot Firmware Signature Database (Policy) | OEM | Flash (Read Only Data), ROM |
| **UDI** | Boot Firmware (BMC, Firmware) | OEM/IHV | Flash (Read Only Data) – staging area |