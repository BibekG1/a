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

