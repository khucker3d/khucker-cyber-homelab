# Full Drive BitLocker Encryption (Windows 11 Pro)
Author: Kellie Hucker  

## Overview:
This project documents enabling full disk encryption using BitLocker on Windows 11 Pro to protect data at rest. BitLocker ensures that sensitive data remains protected if a device is lost, stolen, or accessed outside of a trusted boot environment.

### Objective:
- Encrypt the entire OS drive using BitLocker  
- Protect data at rest from unauthorized access  
- Configure secure key management and recovery options  
- Establish a hardened baseline for a cybersecurity workstation

**Why Encryption Matters:** 
- BitLocker mitigates these risks by enforcing encryption tied to trusted platform integrity.

**Without full disk encryption:**
- Data can be accessed by removing the drive  
- Attackers can boot from external media  
- Sensitive files may be recoverable from unallocated space  

## How To (Summary):
1. Verify TPM Availability: Confirmed TPM is present and ready: `Get-Tpm`
2. Enable BitLocker on the OS drive using system settings or Control Panel.
3. Configure Startup (TPM-based) Protection
   _(Optional) TPM + PIN for increased security._
5. Back up recovery key securely in multiple locations:
   - _Microsoft account_
   - _Offline backup (USB)_
6. Select Full Drive Encryption to protect previously deleted data.
7. Select Encryption Mode: XTS-AES
   _(modern BitLocker encryption mode for fixed drives)_.
8. Initiated encryption and allowed the process to complete while on AC power.
9. Validate Encryption Status: `manage-bde -status C:`

**Results:**
 - Full disk encryption successfully enabled
 - Data at rest is protected against unauthorized access
 - System aligned with security best practices
 - Device ready for secure cybersecurity lab usage

### Operational Considerations
 - Firmware or boot changes may trigger recovery key prompts
 - Always store recovery keys in multiple secure locations
 - Suspend BitLocker before major BIOS or boot changes

## Skills Demonstrated
 - Endpoint security
 - Encryption configuration (BitLocker)
 - Key management and recovery planning
 - OS hardening
 - Risk mitigation for data at rest

## Security Notes
This project is intended for learning, personal security practice, and portfolio demonstration.
