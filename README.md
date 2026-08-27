# 🧬 BacTigen – Automated identification of vaccine candidates from raw protein sequences

BacTigen is a fully automated machine learning‑powered reverse vaccinology platform designed to identify protective antigens and design multi‑epitope vaccine candidates directly from raw bacterial protein sequences.

This repository contains the standalone, portable version of BacTigen – **no R installation is required**.

---

## 📥 Download

**Download the latest stable version from the [Releases](https://github.com/Milad-Norouzi/BacTigen/releases) page.**

The package is distributed as a compressed archive (`.rar`). After downloading, extract it to any folder on your computer.

---

## 📁 Folder Structure

After extracting the package, you will see the following:

BacTigen/
├── BacTigen.lnk # Shortcut to launch the application
├── Tools/ # All application files (R‑Portable, Shiny, dependencies)
├── BacTigen_Outputs/ # (created automatically) Saved analysis results
└── README.md # This file


Everything except the shortcut and the outputs folder is contained inside `Tools/`.

---

## 🚀 How to Run BacTigen

1. **Double‑click** the `BacTigen.lnk` shortcut.
2. Your default web browser will open automatically at:  
   `http://127.0.0.1:4338/`
3. The BacTigen interface will load. You can now upload a FASTA file or paste protein sequences and start the analysis.

> **Important:** The shortcut can be moved **anywhere** on your computer – it will always point back to the application folder.  
> However, **do not move individual files or folders** inside the `Tools/` directory. The application relies on the relative structure to work correctly.

---

## 📂 Where Are the Results Saved?

All analysis outputs are automatically saved in:
BacTigen_Outputs/


Inside this folder, each run creates a new subfolder named either:

- `BacTigen_Result_1`, `BacTigen_Result_2`, … (default)
- or your custom project name (if you entered one in the interface)

Each result folder contains:

- `Final_Report.html` – interactive HTML table with all predictions and hyperlinks
- `Homology/` – BLAST alignment details (linked from the report)
- `Epitopes/` – B‑cell, MHC‑I and MHC‑II epitope tables
- `Multi_Epitopes_Design/` – vaccine construct sequences and FASTA files

---

## 🔗 Important Note About HTML Links

The interactive HTML report (`Final_Report.html`) contains clickable links that open additional files (e.g., BLAST alignments, epitope tables, FASTA sequences).

**For these links to work correctly, you must keep the entire `BacTigen_Outputs` folder together** – do not move individual files out of the folder. If you move the whole `BacTigen_Outputs` folder to another location, the links will still work because they use relative paths.

---

## 🛠️ Requirements

- **Operating System:** Windows 7, 8, 10, or 11 (64‑bit recommended)
- **Browser:** Any modern browser (Chrome, Edge, Firefox)
- **Disk Space:** ~3 GB (includes R‑Portable and dependencies)
- **RAM:** 4 GB minimum (8 GB recommended for large proteomes)
- **No R installation is required** – BacTigen includes its own R‑Portable runtime inside `Tools/`.

---

## ❓ Troubleshooting

| Issue | Solution |
|:---|:---|
| Application does not start | Make sure the `Tools/App/R-Portable/bin/R.exe` file exists. Do not move individual folders inside `Tools/`. |
| Browser does not open automatically | Manually open a browser and go to `http://127.0.0.1:4338/` |
| Report links don't work | Keep the entire `BacTigen_Outputs` folder in its original location. |
| Error about missing dependencies | Run the app from within the extracted folder – do not copy only the `.lnk` file elsewhere. |
| Firewall warning | Allow the connection – BacTigen runs only on your local machine and does not access the internet. |

---

## 📖 How to Cite

If you use BacTigen in your research, please cite:

> [Author names], *BacTigen: A Machine Learning‑Powered Reverse Vaccinology Platform for Protective Antigen Discovery and Multi‑Epitope Vaccine Design from Raw Sequences*, [Journal name, year].

(Full citation details will be provided in the associated publication.)

---

## 📞 Contact & Support

For questions, bug reports, or feature requests, please contact:

- **email@example.com**
- or open an issue on the project’s [GitHub repository](https://github.com/Milad-Norouzi/BacTigen/issues).

---

## ⚠️ Disclaimer

BacTigen is a research tool intended for computational vaccine candidate prioritisation. All predictions should be validated experimentally. The authors are not responsible for any misuse or misinterpretation of the results.

---

**© 2026 – BacTigen – Automated identification of vaccine candidates from raw protein sequences**
