# 💰 Simple Finance Dashboard

A lightweight, interactive finance dashboard built with **Streamlit**, **Pandas**, and **Plotly** for tracking and categorizing expenses from CSV bank statements.

---

## 🚀 Features

- 📤 **Upload CSV** bank statements
- 🏷 **Auto-categorize transactions** using saved keywords (`categories.json`)
- ✏ **Edit categories** directly in the app
- 📊 **View expense summaries** in tables and pie charts
- 💾 **Persistent category storage** for future uploads
- 💡 **Debit & Credit tabs** for quick insights

---

## 📦 Installation

This project uses [`uv`](https://docs.astral.sh/uv/) for fast Python environment & dependency management.

```bash
# 1️⃣ Clone the repository
git clone https://github.com/Manoj-tech25/AutomateFinanceApp.git
cd AutomateFinanceApp

# 2️⃣ Create and activate virtual environment
uv venv
source .venv/bin/activate    # Mac/Linux
.venv\Scripts\activate       # Windows

# 3️⃣ Install dependencies
uv pip install -r requirements.txt

# Run the Streamlit app
streamlit run main.py

#Project Structure
.
├── main.py                   # Main Streamlit app
├── categories.json           # Stores category names & keywords
├── sample_bank_statement.csv # Example input CSV
├── pyproject.toml            # Project metadata
├── README.md                 # This file
└── .gitignore                # Files/folders to ignore in git

#📑 CSV Format

Your bank statement CSV should contain the following columns:

Date	Details	Debit/Credit	Amount
01 Jan 2025	Grocery Store	Debit	150.25
03 Jan 2025	Salary	Credit	5000.00

Date format: %d %b %Y (e.g., 01 Jan 2025)

Amount can have commas, which are auto-cleaned

#💾 Category Storage

Categories and keywords are stored in categories.json automatically.
When you assign a category to a transaction, the "Details" text is saved as a keyword for future matching.