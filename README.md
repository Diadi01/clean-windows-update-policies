# 🧹 Windows Registry Policy Cleaner

## Description

This batch script removes legacy and restrictive Windows registry policy entries that may interfere with:

- Receiving Windows Updates
- Enabling Insider builds
- Accessing Microsoft Store updates

It targets both `HKCU` (user-level) and `HKLM` (system-level) registry paths, including those under:

- `Microsoft\Policies`
- `WindowsSelfHost`
- `WindowsStore\WindowsUpdate`
- `WOW6432Node` mirrors for 32-bit apps on 64-bit systems

## ⚠️ Disclaimer

> **Back up your registry before running this script.**  
> Modifying registry entries can impact system behaviour and stability.  
> This script is provided "as-is" without any warranty or support.

---

## 💻 How to Use

1. **Download the `.bat` file** or clone this repository:
   ```bash
   git clone https://github.com/Diadi01/clean-windows-update-policies.git
2.  **Run the batch file as Administrator**:
- Right-click on clean-windows-update-policies.bat
- Select "Run as administrator"
- Reboot your PC (recommended) to apply changes
3. Here are the key commands used in the script:
   reg delete "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies" /f
   reg delete "HKCU\Software\Microsoft\WindowsSelfHost" /f
   reg delete "HKCU\Software\Policies" /f
   reg delete "HKLM\Software\Microsoft\Policies" /f
   reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Policies" /f
   reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\WindowsStore\WindowsUpdate" /f
   reg delete "HKLM\Software\Microsoft\WindowsSelfHost" /f
   reg delete "HKLM\Software\Policies" /f
   reg delete "HKLM\Software\WOW6432Node\Microsoft\Policies" /f
   reg delete "HKLM\Software\WOW6432Node\Microsoft\Windows\CurrentVersion\Policies" /f
   reg delete "HKLM\Software\WOW6432Node\Microsoft\Windows\CurrentVersion\WindowsStore\WindowsUpdate" /f

  ---

  ✅ **Use Cases**
- Reset Windows Update policies
- Fix broken Insider Preview settings
- Clear out store-related restrictions
- Prepare your system for fresh updates


