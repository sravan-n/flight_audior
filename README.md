# Flight Auditor

## Overview

**Flight Auditor** is a capstone project for the **eCornell - Python Programming Certificate**. This application audits and validates flight operations at a flight school, ensuring compliance with certification requirements, weather minimums, and pilot qualifications.

The system analyzes flight records against pilot certifications, ratings, endorsements, and weather conditions to identify flight violations and generate audit reports.

## Project Details

- **Course**: Python Programming Certificate (eCornell)
- **Project Type**: Capstone Project
- **Language**: Python 3.10+
- **Dependencies**: `python-dateutil`, `pytz`

## Key Topics Covered

This capstone project demonstrates mastery of the following Python programming concepts:

### Python Fundamentals
- Variables, data types, and operators
- String manipulation and formatting
- Input/output operations
- Code organization and best practices

### User-Defined Functions
- Function definition and calling
- Parameters and return values
- Function documentation (docstrings)
- Error handling and exceptions

### Controlling Program Flow
- Conditional statements (`if`, `elif`, `else`)
- Loops (`for`, `while`)
- Loop control (`break`, `continue`)
- Nested control structures

### Mastering Data Structures
- **Lists**: Creation, indexing, slicing, and manipulation
- **Dictionaries**: Key-value pairs, iteration, and lookup
- **Sets and Tuples**: Immutable collections and set operations
- **2D Lists**: Multi-dimensional data handling

### Auditing Datasets
- **Text Files**: Reading and parsing text data
- **CSV Files**: Reading/writing structured data with `csv` module
- **JSON Files**: Parsing and working with JSON objects
- **DateTime Objects**: Working with dates and times
- **Time Zones**: Timezone-aware datetime handling with `pytz`
- **Data Validation**: Ensuring data integrity and correctness

## Project Structure

```
flight_auditor/
├── auditor/                    # Main application package
│   ├── __main__.py            # Entry point
│   ├── app.py                 # Main application logic
│   ├── pilots.py              # Pilot certifications and ratings
│   ├── endorsements.py        # Pilot endorsements handling
│   ├── inspections.py         # Aircraft inspection records
│   ├── violations.py          # Flight violation detection
│   ├── utils.py               # Utility functions
│   └── tests/                 # Unit tests
│       ├── test_app.py
│       ├── test_pilots.py
│       ├── test_endorsements.py
│       ├── test_inspections.py
│       ├── test_violations.py
│       ├── test_utils.py
│       └── [test data CSV/JSON files]
│
├── KITH-2017/                 # Sample flight school data (2017)
│   ├── fleet.csv
│   ├── instructors.csv
│   ├── lessons.csv
│   ├── students.csv
│   ├── repairs.csv
│   ├── minimums.csv
│   ├── weather.json
│   └── daycycle.json
│
├── KITH-2018/                 # Sample flight school data (2018)
└── KITH-2019/                 # Sample flight school data (2019)
```

## Key Modules

### `pilots.py`
Determines pilot certifications, ratings, and endorsements at the time of flight.
- **Certifications**: NOVICE, STUDENT, CERTIFIED, 50_HOURS, INVALID
- **Ratings**: Instrument Rating
- **Endorsements**: Advanced (retractable gear), Multiengine
- **Functions**: 
  - `get_certification()` - Returns pilot certification level
  - `has_instrument_rating()` - Checks instrument rating
  - `has_advanced_endorsement()` - Checks advanced endorsement
  - `has_multiengine_endorsement()` - Checks multiengine endorsement
  - `get_minimums()` - Returns flight minimums based on pilot qualifications

### `violations.py`
Detects flight violations based on pilot qualifications and weather conditions.

### `inspections.py`
Manages aircraft inspection records and maintenance history.

### `endorsements.py`
Handles pilot endorsements and special permissions.

### `utils.py`
General-purpose utility functions including:
- CSV reading/writing
- JSON parsing
- Time/date conversions
- Data validation

### `app.py`
Main application logic that orchestrates the audit process.

## Installation

### Prerequisites
- Python 3.10 or higher
- pip (Python package manager)

### Setup

1. Clone or download the project:
```bash
cd flight_auditor
```

2. Install dependencies:
```bash
pip install python-dateutil pytz
```

## Running the Application

### Run the entire audit:
```bash
python -m auditor
```

### Run specific modules:
```bash
# Run pilots module
python -m auditor.pilots

# Run violations module
python -m auditor.violations
```

## Running Tests

Run all unit tests:
```bash
python -m pytest auditor/tests/
```

Run specific test file:
```bash
python -m pytest auditor/tests/test_pilots.py
```

## Data Files

The project includes flight school data from multiple years (KITH-2017, KITH-2018, KITH-2019) with the following CSV files:

- **fleet.csv** - Aircraft in the school's fleet
- **students.csv** - Student pilots
- **instructors.csv** - Flight instructors
- **lessons.csv** - Flight lessons performed
- **minimums.csv** - Flight weather/ceiling minimums
- **repairs.csv** - Aircraft maintenance records
- **weather.json** - Weather conditions by date
- **daycycle.json** - Sunrise/sunset times for determining day/night

## Features

✅ Pilot certification validation
✅ Rating and endorsement tracking
✅ Weather minimum compliance checking
✅ Flight violation detection
✅ Multi-year audit support
✅ Comprehensive test suite
✅ Timezone-aware datetime handling

## Configuration

Configure the Python environment in VS Code by editing `.vscode/settings.json`:

```json
{
    "python.defaultInterpreterPath": "/opt/anaconda3/bin/python"
}
```

Or use the Settings UI (`Cmd + ,`) and search for "Python: Default Interpreter Path".

## License

This is an educational project created as part of the eCornell Python Programming Certificate program.

## Author

Developed as a capstone project for eCornell Python Programming Certificate.
