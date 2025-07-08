# Invoice Generation Project

This project automates the process of generating PDF invoices from Excel files.

## Project Structure

- `main.py`: Main script that reads Excel files and generates PDF invoices.
- `invoice/`: Folder containing Excel invoice files (`.xlsx`).
- `pdf/`: Output folder for generated PDF invoices.


## How It Works

1. The script scans the `invoice/` directory for all `.xlsx` files.
2. For each Excel file:
   - Reads invoice data using pandas.
   - Extracts invoice number and date from the filename.
   - Creates a PDF invoice using the FPDF library.
   - Adds a table with product details and a total sum.
   - Saves the PDF to the `pdf/` directory.

## Requirements

- Python 3.12
- pandas
- fpdf

Install dependencies with:

```sh
pip install pandas fpdf
```

## Usage

Run the script:

```sh
python main.py
```

PDF invoices will be generated in the `pdf/` folder, matching the names of the Excel files in `invoice/`.

## Example

- Input: `invoice/2. 10001-2023.1.18.xlsx`
- Output: `pdf/2. 10001-2023.1.18.pdf`