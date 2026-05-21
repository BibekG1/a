# 📖 WINDOWS and OFFICE ACTIVATOR - 1

## ⚠️ Important Disclaimer
This document and the associated script are provided **strictly for educational, development, and system administration study purposes**. it demonstrates how Windows Software Protection Platform (SPP), KMS volume licensing mechanisms, and activation renewal tasks interact at the OS level. It is not intended for production use, redistribution, or circumvention of legitimate software licensing. Always comply with Microsoft's End User License Agreement (EULA) and applicable laws in your jurisdiction.

---

## 🖥️ Supported Operating Systems & Build Requirements

| Feature                 | Supported OS                              | Minimum Build | Notes                                  |
|-------------------------|-------------------------------------------|---------------|----------------------------------------|
| **HWID Activation**     | Windows 10 / 11 (Client & Server)         | 10240+        | Requires one-time internet contact.    | 
| **KMS38 Activation**    | Windows 10 / Server 2016+                 | 14393+        | Offline-capable. Valid until Jan 2038. |
| **Online KMS**          | Windows 7 / 8 / 8.1 / 10 / 11 & Servers   | 7600+         | Requires internet for KMS handshake.   |
| **Office Activation**   | Office 2010, 2013, 2016, 2019, 2021, 365  | Varies        | Handles Retail ↔ Volume conversion.    |
| **Scheduled Renewal**   | Windows Vista / 7 / 8 / 10 / 11           | 6000+         | Uses Windows Task Scheduler.           |

ㅤ
> .

ㅤ
>
> 📌 **Note:** Unsupported builds will exit gracefully with a version-check warning.
> 
ㅤ
ㅤ
> .
ㅤ
 


| Feature                 |  Persistence & Upgrades                                                                                                |
|-------------------------|------------------------------------------------------------------------------------------------------------------------|
| **HWID Activation**     | Permanent: Tied to hardware; survives restarts, updates, resets, and clean OS installs.                                | 
| **KMS38 Activation**    | Semi-Permanent: Survives restarts/updates; resets if you clean-reinstall the OS.                                       |
| **Online KMS**          | Temporary: But Indefinite (via Task) auto-renews forever. Survives restarts, but wiped by major upgrades or PC resets. |
| **Office Activation**   | Varies: Survives restarts; major updates or PC resets will break the activation.                                       |
| **Scheduled Renewal**   | Temporary: Survives restarts, but major Windows upgrades or PC resets will wipe the scheduled task.                    |


---

## 📦 Core Features & Modules

| Option | Functionality                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `[A]`  | **HWID Activation** – Triggers Windows digital license via hardware hash sync.                                              | 
| `[B]`  | **KMS38 Activation** – Applies built-in KMS GVLK + local activation (2038 expiry).                                          | 
| `[C]`  | **Online KMS** – Connects to KMS servers for Windows/Office. Includes auto-renewal task creation.                           | 
| `[D]`  | **Check Activation Status** – Queries `slmgr.vbs -xpr`, WMIC SPP classes, and license states.                               | 
| `[E]`  | **Extras** – `$OEM$` folder generation, key injection, retail-to-volume conversion, task management, and script extraction. |


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

