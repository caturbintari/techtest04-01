# QA Technical Test - Automation Framework

This project shows the solution to the Quality Assurance technical test by Caturiani Pratidina Bintari using Python Playwright.

## Project Overview

The framework covers three key requirements:

1.  **API Automation**: API automation testing with 5 scenarios
2.  **Website test Automation**: Website functionality automation testing (5 positive and 5 negative scenarios)
3.  **Data generation script**: Fetches user data from `reqres.in` and exports it to a CSV file using a specific manual formatting logic

---

## Tech Stack & Prerequisites

- **Language**: Python 3.8+
- **Web Automation**: Playwright
- **API Interaction**: Requests
- **Reporting**: Allure Report
- **Test Runner**: Pytest

### ⚠️ Important: Allure Report Requirement

> **Disclaimer:** To generate and view the actual HTML visualization report, you must have **Java (JDK 8+)** and the **Allure Commandline** tool installed on your system.
>
> - **Windows:** `scoop install allure` (or download binary manually)
> - **Mac:** `brew install allure`
> - **Linux:** `sudo apt-get install allure`

---

## Setup & Installation

Follow these steps to set up the environment:

### 1. Clone or Download Project

Open your terminal in the project directory

### 2. Create Virtual Environment (Recommended)

Isolate dependencies by creating a virtual environment:

- **Windows:**
  ```bash
  python -m venv venv
  venv\Scripts\activate
  ```
- **Mac / Linux:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### 3. Install Dependencies

Install the required Python packages (`requests`, `playwright`, `pytest`):

```bash
pip install requests playwright pytest pytest-html

```

### 4. Install Playwright Browsers

Download the necessary browser binaries (Chromium, Firefox, Webkit):

```bash
playwright install

```

---

## How to Run

### 1. Run Automation Tests (API & UI)

To execute the full test suite:

```bash
pytest"

```

**Run specific modes:**

- **Run with visual browser (Headed mode):**

```bash
cd ..folder
pytest test_01_status.py

```

### 2. Run Data Generation Script

To generate the CSV file from the API:

```bash
cd ..convert06
python additional.py

```

- **Output:** A file named `response.csv` will be created in the root folder.

- **Note:** This script uses a custom manual string builder for CSV generation as per the technical test reference.

---

## Project Structure

```text
/techtest04-01
├── __pycache__/
├── .pytest_cache/
├── allure-results/
├── api/                   # API automation test suite
│   ├── test_01_status.py
│   └── test_02_latency.py
│   ├── test_03_schema.py
│   └── test_04_dataval.py
│   ├── test_05_format.py
│
├── conver06/              # Additional test
│   ├── additional.py      # Main script for Data Generation (CSV)
│
├── website/               # Website automation test suite
│   ├── test_negative.py   # 5 negative scenario
│   └── test_positive.py   # 5 positive scenario
│   └── test_positive.py   # 5 positive scenario
│
├── README.md              # Documentation
├── requirements.txt       # Python dependencies



```

---

_Submitted for Technical Test. By, Caturiani Pratidina Bintari_
