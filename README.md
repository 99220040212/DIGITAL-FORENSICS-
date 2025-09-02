# DIGITAL-FORENSICS-
Lab experiments 
# Ex. No. 1: Evidence Acquisition Using AccessData FTK Imager  

**Date:** 2 

---

## Description  

Forensic Toolkit (FTK) is a computer forensics software product made by AccessData.  
It is a Windows-based commercial product, but a free version with fewer functionalities is also available.  

**FTK Imager** is capable of both acquiring and analyzing forensic evidence.  

The evidence acquired can be divided into two categories:  

- **Volatile Memory Acquisition** (RAM)  
- **Non-Volatile Memory Acquisition** (Hard Disk)  

---

## Methods of Usage  

There are two possible ways to use FTK Imager for forensic image acquisitions:  

1. **Portable Version**  
   - Run FTK Imager from a USB drive or external HDD.  
   - Commonly used for **live data acquisition** when the evidence system is powered on.  

2. **Installed Version**  
   - Install FTK Imager on the investigator’s laptop.  
   - Connect the suspect’s disk using a **write blocker** to prevent modifications and ensure data integrity.  

---

## Acquiring Volatile Memory (RAM)  

FTK Imager can collect the complete volatile memory of a computer.  

**Steps:**  
1. Open FTK Imager.  
2. Navigate to the volatile memory icon (**Capture Memory**).  
3. Choose options as needed:  
   - **Pagefile** (`pagefile.sys`) – Used as virtual memory in Windows, may contain valuable data.  
   - **AD1 file** – FTK’s proprietary image format, useful for later analysis.  
4. Click **C**
