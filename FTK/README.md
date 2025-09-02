## *Ex. No. 1 – Evidence Acquisition Using AccessData FTK Imager*

## 📖 Overview
FTK Imager is a forensic software tool developed by **AccessData**.  
- **Platform**: Windows-based commercial product.  
- **Versions**:  
  - Commercial version with full features.  
  - Free version with limited functionalities.  
- **Capabilities**:  
  - Acquire and analyze forensic evidence.  
  - Supports both **volatile memory** (RAM) and **non-volatile memory** (disks).  

---

## 🧩 Methods of Using FTK Imager
1. **Portable Version**  
   - Run directly from USB/HDD.  
   - Used for **live data acquisition** (evidence machine powered on).  

2. **Installed on Investigator’s Laptop**  
   - Source disk connected via **write blocker** (ensures read-only access, maintains integrity).  

---

## 🧠 Acquiring Volatile Memory
Steps:
- Open FTK Imager → Select **Capture Memory**.  
- Options:  
  - **Pagefile.sys**: Used as virtual memory, may contain valuable evidence.  
  - **AD1 file**: FTK proprietary image format for later use.  
- Output:  
  - Acquired memory saved with extension **`.mem`**.  

---

## 💾 Acquiring Non-Volatile Memory (Disk Imaging)
Steps:
1. Open FTK Imager → **Create Disk Image**.  
2. Select source:  
   - **Physical drives**  
   - **Logical drives/partitions**  
   - **Image files**  
   - **Folders / CDs / DVDs**  
3. Choose image format:  
   - **Raw (dd)** → Most common, no metadata, includes padding.  
   - **SMART** → Linux-specific, structured with headers/sections.  
   - **E01 (EnCase)** → Proprietary, compressed, includes metadata + MD5 hash.  
   - **AFF/AFF4** → Open forensic format, non-proprietary.  

---

## 📝 Case Information & Image Details
- Input case details (examiner, notes, timestamps).  
- Configure:  
  - **Image Destination** → Save path.  
  - **File Name**  
  - **Fragment Size**:  
    - `0` = single large file.  
    - Non-zero = fragmented files.  
- Select **Verify images after creation** (hash check).  
  - Ensures data integrity, though acquisition time increases.  

---

## ✅ Output & Verification
- After acquisition, FTK generates:  
  - **Disk image files** in chosen format.  
  - **Text report** with acquisition details.  
- Hash values are verified to confirm **data integrity**.  

---

# 🧾 Key Takeaways
- FTK Imager supports **both live (volatile) and offline (disk) evidence acquisition**.  
- Use of **write blockers** is critical for forensic integrity.  
- **Different formats** (Raw, E01, AFF, SMART) serve different investigative needs.  
- Always **verify acquired images with hash values** to ensure admissibility in court.  
