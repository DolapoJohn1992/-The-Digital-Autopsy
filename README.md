# Digital Autopsy: Malware Investigation Report

## Overview
This repository contains the forensic documentation for a malware investigation conducted on a compromised disk image and a raw memory dump. The investigation identifies the threat actor, the malicious files involved, the infection timeline, and the persistence mechanism.

## Investigation Findings

* **Who**: The threat actor identified is TitanCorp.
* **What**: The primary malicious file discovered was `_ESUME.EXE`, which was identified as a deleted file.
* **When**: The infection event occurred on 2026-05-21.
* **How**: Persistence was achieved using `rootkit_beacon.exe`, which was found running as a hidden process with PID 4444.

## Methodology
The investigation utilized the following forensic approach:
1. **Disk Analysis**: Used `istat` to inspect file system metadata and identify deleted entries.
2. **Memory Analysis**: Used `strings` combined with `grep` to parse the memory dump for malicious process strings, specifically targeting `rootkit_beacon.exe`.
3. **Documentation**: Findings were consolidated into a formal markdown report.
