<!--- @file
  Summary.md for Understanding the UEFI Secure Boot Chain

  Copyright (c) 2019, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

-->

# Summary

* [Understanding UEFI Secure Boot Chain](README.md)
* [Executive Summary](executive_summary.md)
* [Overview](overview.md)
* [Secure Boot Chain in UEFI](secure_boot_chain_in_uefi/README.md)
  * [UEFI Secure Boot](secure_boot_chain_in_uefi/uefi_secure_boot.md)
  * [Intel® Boot Guard](secure_boot_chain_in_uefi/intel_boot_guard.md)
  * [Boot Chain – Putting it all together](secure_boot_chain_in_uefi/boot_chain__putting_it_all_together.md)
  * [Signed Recovery](secure_boot_chain_in_uefi/signed_recovery.md)
  * [S3 Resume](secure_boot_chain_in_uefi/s3_resume.md)
  * [SMM Runtime Communication](secure_boot_chain_in_uefi/smm_runtime_communication.md)
* [Additional Secure Boot Chain Implementations](additional_secure_boot_chain_implementations/README.md)
  * [Machine Owner Key \(MOK\)](additional_secure_boot_chain_implementations/machine_owner_key_mok.md)
  * [coreboot](additional_secure_boot_chain_implementations/coreboot.md)
  * [Android Verified Boot](additional_secure_boot_chain_implementations/android_verified_boot.md)
* [Looking Forward – Platform Firmware Resiliency](looking_forward__platform_firmware_resiliency/README.md)
  * [Platform Firmware Resiliency](looking_forward__platform_firmware_resiliency/platform_firmware_resiliency.md)
  * [Device Firmware Boot](looking_forward__platform_firmware_resiliency/device_firmware_boot.md)
  * [Device Firmware Update](looking_forward__platform_firmware_resiliency/device_firmware_update.md)
  * [Project Cerberus](looking_forward__platform_firmware_resiliency/project_cerberus.md)
  * [Intel® Platform Firmware Resilience \(Intel® PFR\)](looking_forward__platform_firmware_resiliency/intel_platform_firmware_resilience_intel_pfr.md)
  * [Google Titan](looking_forward__platform_firmware_resiliency/google_titan.md)
  * [Other Platform Firmware Resiliency \(PFR\) Implementations](looking_forward__platform_firmware_resiliency/other_platform_firmware_resiliency_pfr_implementat.md)
* [Glossary](glossary.md)
* [References](references.md)

## Figures

* [Figure 1-1: Clark-Wilson model, From Lee](overview.md#clark-wilson-model-from-lee)
* [Figure 2-1: UEFI Secure Boot ](secure_boot_chain_in_uefi/uefi_secure_boot.md#2-1-uefi-secure-boot)
* [Figure 2-2: Image Verification flow](secure_boot_chain_in_uefi/uefi_secure_boot.md#2-2-image verification flow)
* [Figure 2-3: Image Verification with timestamp signature database](secure_boot_chain_in_uefi/uefi_secure_boot.md#2-3-image-verification-with-timestamp-signature-database)
* [Figure 2-4: Intel® Boot Guard diagram credit CYBER-RESILIENCY IN CHIPSET AND BIOS](secure_boot_chain_in_uefi/intel_boot_guard.md#2-4-intel-boot-guard-diagram-credit-cyber-resiliency-in-chipset-and-bios)
* [Figure 2-5: Secure Boot Verification Flow](secure_boot_chain_in_uefi/boot_chain__putting_it_all_together.md#2-5-secure-boot-verification-flow)
* [Figure 2-6: Intel® BIOS Guard](secure_boot_chain_in_uefi/boot_chain__putting_it_all_together.md#2-6-intel-bios-guard)
* [Figure 3-1: Linux MOK Boot, source: UEFI Secure Boot Webinar](additional_secure_boot_chain_implementations/machine_owner_key_mok.md#3-1-linux-mok-boot-source-uefi-secure-boot-webinar)
* [Figure 3-2: coreboot Verified Boot source: “Verified Boot in Chrome OS and how to make it work for you"](additional_secure_boot_chain_implementations\coreboot.md#3-2-coreboot-verified-boot-source-verified-boot-in-chrome-os-and-how-to-make-it-work-for-you)




