# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report

<img width="704" height="580" alt="Screenshot 2025-09-24 151948" src="https://github.com/user-attachments/assets/b6b583df-c3fb-41a0-b32f-3c0a8148a596" />

<img width="1340" height="985" alt="Screenshot 2025-09-24 152337" src="https://github.com/user-attachments/assets/34a70492-aafc-45ea-a5b0-6acb200ea130" />

<img width="1289" height="494" alt="Screenshot 2025-09-24 152424" src="https://github.com/user-attachments/assets/a0dcedea-1e3b-4ce3-9c84-5002477f87fa" />


<img width="1917" height="1079" alt="Screenshot 2025-09-24 152448" src="https://github.com/user-attachments/assets/a8b2dbbc-c1be-498a-b4cb-9daa6d2f4caa" />

<img width="1919" height="1079" alt="Screenshot 2025-09-24 152506" src="https://github.com/user-attachments/assets/2666f5cd-2431-4907-bd3e-ace974d3c49a" />

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

