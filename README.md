# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details

# Install and Verify Steghide Tool

<img width="882" height="619" alt="image" src="https://github.com/user-attachments/assets/5671976a-beeb-4f89-8a2c-eca2ee0a47ba" />

# Embed the Secret Message into the Image

<img width="514" height="91" alt="image" src="https://github.com/user-attachments/assets/67de6700-8a1a-4716-aee1-542cb27ee18a" />

# Extract the Hidden Secret from Image
<img width="566" height="89" alt="image" src="https://github.com/user-attachments/assets/3a8ada65-9949-46df-adf4-0d03672ecd65" />

# Verify the Extracted Message
<img width="340" height="60" alt="image" src="https://github.com/user-attachments/assets/eee800eb-49c8-477b-b1f1-b7bf2b6b12ce" />

# Retrieve Information About the Embedded Data
<img width="523" height="188" alt="image" src="https://github.com/user-attachments/assets/466e1ddb-392b-4624-b11a-25a67f9f321c" />

# Analyze File Signature

<img width="1248" height="77" alt="image" src="https://github.com/user-attachments/assets/52c744f9-a2a7-4e51-9388-d204a143efe6" />

<img width="727" height="120" alt="image" src="https://github.com/user-attachments/assets/1de90af7-ad7e-4730-a846-ed49c57e50c7" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
