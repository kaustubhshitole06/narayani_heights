# Food Items Document Processor

This script processes a list of food items from a DOCX file and creates a beautifully formatted Word document with a professional food items template.

## Features

- Reads items from an input DOCX file (one item per line)
- Creates a new formatted Word document
- **2 items per page** with professional template
- Each item includes:
  - Item number and name
  - Category field
  - Description field
  - Price field
  - Ingredients field
  - Allergens field
  - Serving size field
  - Additional notes section

## Requirements

Install the required package:

```bash
pip install python-docx
```

## Usage

1. Prepare your input DOCX file with a list of food items (one per line)
2. Run the script:
   ```bash
   python process_food_items.py
   ```
3. Enter the path to your input file when prompted
4. Enter the desired output file name (or press Enter for default)

## Example

**Input file (sample_items.docx):**
```
Pizza
Burger
Pasta
Salad
```

**Output:** A formatted Word document with a title page, then 2 items per page with complete food item templates ready to be filled in.

## Template Structure

Each food item includes:
- Centered heading with item number
- Bold, colored item name
- Formatted table with fields for food details
- Notes section for additional information
- Professional styling and spacing
