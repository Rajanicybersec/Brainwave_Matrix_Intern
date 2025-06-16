# 🛡️ Malware Detection Tool

A Python-based malware detection tool that scans files for suspicious indicators using static analysis and SHA-256 hashing. This project is developed as part of an internship task to demonstrate practical skills in basic malware analysis.

---

## 🚀 Features

- 🔍 **File Scanning**: Automatically scans files in a specified directory.
- 🔐 **SHA-256 Hashing**: Calculates a unique hash for file identification and integrity checking.
- ⚠️ **Static Analysis**: Flags suspicious patterns commonly found in malicious scripts, such as:
  - `os.system`, `subprocess`, `eval`
  - Network commands like `wget`, `curl`
  - Obfuscation techniques like `base64`, `powershell`
- 📂 **Modular Code Structure**: Organized for easy understanding and extension.

---

## 📁 Project Structure

```
malware_detector/
├── scanner.py               # Main scanning script
├── utils/
│   ├── hash_utils.py        # SHA-256 hashing logic
│   └── static_analysis.py   # Suspicious pattern detection
├── samples/                 # Test files (malicious & clean)
├── reports/                 # Optional report storage
├── README.md                # Project documentation
└── requirements.txt         # Required Python libraries
```

---

## 🛠️ How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/Rajanicybersec/Brainwave_Matrix_Intern/
cd malware_detector
```

### 2. Set Up Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Add Files to Scan
Place `.py`, `.sh`, `.exe`, or `.txt` files inside the `samples/` folder.

### 4. Run the Tool
```bash
python scanner.py
```

---

## 📄 Sample Output

```
[+] Scanning: samples/malicious1.py
SHA-256 Hash: 3c1f87e55a9e4b...
Suspicious Indicators Found:
 - Suspicious keyword found: 'os.system'
 - Suspicious keyword found: 'cmd.exe'
```

```
[+] Scanning: samples/clean1.py
SHA-256 Hash: 9ad7f982aa8d2...
No immediate issues found.
```

---

## 🧪 Sample Test Files

| Filename        | Description                                |
|----------------|--------------------------------------------|
| malicious1.py   | Contains `os.system("cmd.exe")`            |
| clean1.py       | Contains `print("This is a test script for malware scanning.")` |

---

## 📌 Notes

- This tool uses **static analysis** only. It does not execute the files.
- Only safe test samples should be used. Do **not** run real malware on your local machine.
- For advanced detection, consider integrating **VirusTotal API** or using behavioral analysis in a VM.

---

## 👩‍💻 Author

**S. Rajani**  
📍 Bangalore, India  
🔗 [LinkedIn](https://www.linkedin.com/in/rajani-s-16a94b301/)  
🔗 [GitHub](https://github.com/Rajanicybersec)

---

## 📜 License

This project is for educational and internship purposes only. Not intended for real-world malware analysis in production.