# Investment Portfolio Script

This project is a Python script designed to process investment portfolio data for dividend calculations, stock analysis, and order creation. The script handles data from a CSV file or downloads it automatically if not available locally.

## Features

- **Dynamic Data Loading**:
  - Reads portfolio data from a CSV file.
  - Automatically downloads the file if not available locally.

- **Investment Calculations**:
  - Calculates the required number of shares to meet a funding goal.
  - Computes income or loss based on dividend data.

- **Customizable**:
  - Adjust funding goals, file paths, and more to suit your needs.

## Requirements

- Python 3.8 or higher
- Libraries:
  - `pandas`
  - `numpy`
  - `requests`
  - `tabulate` (optional, for pretty-printing)

## Setup

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv respvenv
   source respvenv/bin/activate  # For macOS/Linux
   respvenv\Scripts\activate     # For Windows
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the script:
   ```bash
   python investment_script.py
   ```

2. The script will:
   - Load the `downloaded_data.csv` file (or download it automatically).
   - Calculate required shares (`required`) and potential income/loss (`incomeloss`).
   - Print the first row of sorted data with an order recommendation.

## Example Output

```plaintext
CREATE Order: Sell AAPL:10 @ $123.45 for proceeds of $1,234.50
```

## Project Structure

```plaintext
project-folder/
├── investment_script.py    # Main Python script
├── downloaded_data.csv     # CSV file with stock data (auto-downloaded if missing)
├── .gitignore              # Excludes unnecessary files
├── requirements.txt        # Python dependencies
├── respvenv/               # Virtual environment (ignored by Git)
└── README.md               # Project documentation
```

## Configuration

- **Funding Goal**:
  Modify the `fundsneeded` variable in `investment_script.py`:
  ```python
  fundsneeded = 5300  # Example goal
  ```

- **CSV File URL**:
  Update the URL for downloading the CSV file:
  ```python
  url = "https://script.google.com/macros/s/.../exec"
  ```

## Contributions

Contributions are welcome! Feel free to fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
