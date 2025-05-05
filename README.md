# 📄 PDF Data Extraction with Tabula

This project demonstrates how to extract tabular data from PDF files using the **Tabula** library in Python.  
The provided example reads a PDF file and converts a specified page into a CSV format.

---

## 📑 Table of Contents

- [Installation](#installation)  
- [Usage](#usage)  
- [Example Code](#example-code)  
- [Requirements](#requirements)  
- [License](#license)

---

## 🚀 Installation

To use this project, ensure you have Python installed.  
Then, install the required library:

```bash
pip install tabula-py
```

⚠ **Note:** You also need to have Java installed, as Tabula runs on Java.

---

## 💻 Usage

1️⃣ Place your target PDF file in the project directory.  

2️⃣ Run the Python script to extract tables.

---

## 📂 Example Code

```python
import tabula

# Specify your PDF file path
pdf_path = "your_file.pdf"

# Read tables from the PDF (first page by default)
tables = tabula.read_pdf(pdf_path, pages='1', multiple_tables=True)

# Convert each table to CSV
for i, table in enumerate(tables):
    csv_filename = f"output_table_{i + 1}.csv"
    table.to_csv(csv_filename, index=False)
    print(f"Saved {csv_filename}")
```

✅ **Key Points**:
- `pages='1'`: reads the first page; change to `'all'` to extract from all pages.
- `multiple_tables=True`: extracts all tables from the page.

---

## 📦 Requirements

- Python 3.x  
- Java (installed and in your system path)  
- `tabula-py` library

Install dependencies:

```bash
pip install tabula-py
```

---

## 📝 License

This project is licensed under the MIT License.

---

💡 **Tip:** For large or complex PDFs, you can adjust Tabula options like `area`, `guess`, or `lattice` for better extraction accuracy.

---

Happy data extracting! 🚀
