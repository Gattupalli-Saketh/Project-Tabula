# PDF Data Extraction with Tabula

This project demonstrates how to extract tabular data from PDF files using the Tabula library in Python. The example provided reads a PDF file and converts the specified page into a CSV format.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Example Code](#example-code)
- [Requirements](#requirements)
- [License](#license)

## Installation

To use this project, you need to have Python installed on your machine. You can install the required libraries using pip. Run the following command:

```bash
pip install tabula-py

'''markdown
import tabula
'''
#Reads the PDF or Loads the data
file = tabula.read_pdf"Your pdf file" 