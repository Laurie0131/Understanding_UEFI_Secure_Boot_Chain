## Android Verified Boot {#android-verified-boot}

The Android verified boot solution, like UEFI Secure Boot, is used to verify the integrity of an OS image.

_“Verified Boot strives to ensure all executed code comes from a trusted source (usually device OEMs), rather than from an attacker or corruption. It establishes a full chain of trust, starting from a hardware-protected root of trust to the bootloader, to the boot partition and other verified partitions including system, vendor, and optionally OEM partitions. During device boot up, each stage verifies the integrity and authenticity of the next stage before handing over execution.”_

_-- “Verified Boot” ([source.android.com](https://source.android.com/security/verifiedboot))_

![C:\Users\jyao1\Desktop\20180607105827101.png](media/image11.png)

Figure 3-3: Android Verified Boot 1.0 without A/B (source: [Android Verified Boot 2.0](https://blog.csdn.net/rikeyone/article/details/80606147))

![C:\Users\jyao1\Desktop\20180607105904931.png](media/image12.png)

Figure 3-4: Android Verified Boot 1.0 with A/B (source: [Android Verified Boot 2.0](https://blog.csdn.net/rikeyone/article/details/80606147))

![C:\Users\jyao1\Desktop\20180607105927467.png](media/image13.png)

Figure 3-5: Android Verified Boot 2.0 (source: [Android Verified Boot 2.0](https://blog.csdn.net/rikeyone/article/details/80606147))

For additional information on OS kernel verification, see the following:

*   [https://source.android.com/security/verifiedboot](https://source.android.com/security/verifiedboot)

*   [https://android.googlesource.com/platform/external/avb/+/master/README.md](https://android.googlesource.com/platform/external/avb/+/master/README.md)

[https://blog.csdn.net/rikeyone/article/details/80606147](https://blog.csdn.net/rikeyone/article/details/80606147)