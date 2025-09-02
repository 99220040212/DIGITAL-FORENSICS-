## *Ex. No. 5 – Using Autopsy to Create a Case and Import Evidence*

## 📖 Overview
**Autopsy** is an open-source **digital forensics platform** used for analyzing and extracting data from digital devices.  
It supports disk images, file systems, and live analysis, making it a widely used forensic tool.

---

## 🧩 Steps in Using Autopsy

### 1. Installation
- Download Autopsy from the official website.  
- Install according to OS (Windows, Linux, macOS).  

---

### 2. Starting a New Case
- Launch Autopsy → **New Case**.  
- Provide:  
  - Case name  
  - Case storage location  
  - Case number  
  - Examiner details  
- Click **Next** to proceed.  

---

### 3. Adding a Data Source
- Select data source type:  
  - Disk image (`.E01`, `.dd`, `.raw`)  
  - Directory  
  - Logical files  
  - Local disks  
- Browse and select the source file or device.  
- Configure **Ingest Modules** (e.g., File Type Identification, Keyword Search, Hash Lookup).  
- Start analysis.  

---

### 4. Initial Analysis & Overview
- **Ingest Progress** visible in status bar.  
- Autopsy categorizes findings into:  
  - Web artifacts  
  - File system metadata  
  - Communication records  
- **Tree Viewer** allows navigation by:  
  - File System  
  - Web History  
  - Emails  
  - Other artifacts  

---

### 5. Detailed Analysis
- **Keyword Search**:  
  - Use built-in lists or custom keywords.  
- **File Analysis**:  
  - Navigate file system, open/view/export files.  
