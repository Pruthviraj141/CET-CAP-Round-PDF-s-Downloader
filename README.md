# CAP Round PDFs Downloader & Merger

This project provides a simple Bash script to **download all CAP Round 2 PDFs** from the official server and then merge them into a single file using **WSL (Windows Subsystem for Linux)**.

---

## 🚀 Features
- Downloads all CAP Round PDFs (IDs **1000–2000**).
- Saves them into `D:\pdfs`.
- Merge all PDFs into a single file (`merged.pdf`).

---

## 📂 Project Structure
```
📦 cap-round2-pdfs
 ┣ 📜 download_pdfs.sh   # Script to download PDFs
 ┣ 📜 README.md           # Documentation
```

---

## ▶️ Run Script

Open **WSL terminal** and run:

```bash
bash download_pdfs.sh
```

This will download all available CAP Round 2 PDFs into `D:\pdfs`.

---

## 📑 Merge All PDFs into One

After downloading, run this command inside WSL:
Provide Your Drive letter here is D: 
```bash
cd /mnt/d/pdfs
pdftk *.pdf cat output merged.pdf
```

or (if using `pdfunite`):

```bash
pdfunite *.pdf merged.pdf
```

Now you’ll have a single `merged.pdf` file in `D:\pdfs`.

---

## 🔧 Requirements
- **WSL** (Windows Subsystem for Linux)
- `wget` (for downloading)
- Either `pdftk` or `poppler-utils` (for merging PDFs)

Install them inside WSL:

```bash
sudo apt update && sudo apt install wget pdftk poppler-utils -y
```



