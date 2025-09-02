## *Ex. No. 2 – Recover Deleted or Damaged Files Using TestDisk*

## 📖 Aim
Use **TestDisk** step by step to:  
- Recover a **missing partition**  
- Repair a **corrupted partition**  

---

## 🧩 TestDisk Workflow

### 1. Log Creation
- TestDisk lists all connected drives with their correct sizes.  
- Select the target drive (preferably `/dev/rdisk*` for faster transfer).  

---

### 2. Partition Table Detection
- TestDisk auto-detects the **partition table type**.  
- Usually, the default value is correct.  
- Press **Enter** to proceed.  

---

### 3. Analyse Partition Structure
- Use **Analyse** menu → Displays current partition structure.  
- Look for errors such as:  
  - Duplicate partitions → corrupted/invalid entry.  
  - Invalid NTFS boot sector → corrupted filesystem.  
- Proceed with **Quick Search**.  

---

### 4. Quick Search
- Displays results in real time.  
- Missing partitions may appear (e.g., “Partition 3”).  
- Highlight a partition → Press **p** to list files.  
  - Files in red = deleted entries.  
- If partitions look valid → Proceed.  
- If a partition is still missing → Use **Deeper Search**.  

---

### 5. Deeper Search
- Scans cylinders for additional partitions.  
- Detects:  
  - FAT32 backup boot sector  
  - NTFS backup superblock  
  - ext2/ext3 backup superblock  
- Results may show overlapping or damaged partitions.  

✅ Steps:  
- Check partitions marked **D (Deleted)**.  
- Use **p** to list files → verify correct partition.  
- Mark the correct partition as **L (Logical)** or **P (Primary)**.  
- Leave damaged partitions marked as **D (Deleted)**.  

---

### 6. Partition Table Recovery
- Once all correct partitions are identified:  
  - Confirm with **Write → Enter → y → OK**.  
- Partitions are now registered in the partition table.  

---

### 7. NTFS Boot Sector Recovery
- If a boot sector is damaged but a valid backup exists:  
  - Choose **Backup BS** to copy backup sector over damaged one.  
  - Confirm with **y** and **OK**.  
- Status should change to:  
  - **Boot sector OK**  
  - **Backup boot sector OK**  

---

### 8. Final Step
- TestDisk confirms recovery success.  
- Message: **“You have to restart your Computer to access your data.”**  
- Reboot required to complete recovery.  

---

## ✅ Key Takeaways
- **Quick Search** → finds most missing partitions.  
- **Deeper Search** → necessary for severe corruption cases.  
- Always verify partitions by listing files (**p**).  
- Mark partitions correctly (Primary, Logical, Deleted).  
- Use **Write** only when the correct structure is confirmed.  
- NTFS boot sectors can be restored using backups.  
- Final step always requires a **system reboot**.  
