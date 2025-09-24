# FIT2107_D1
## System A## System Architecture


```
src/
├── client.py          # Client entity and management
├── trainer.py         # Trainer entity and management 
├── session.py         # Session entity and types
├── booking_system.py  # Core booking logic
├── membership.py      # Membership rules and validation
├── schedule.py        # Schedule management and conflicts
└── main.py           # Main application interface


tests/
├── test_client.py     # Client management tests
├── test_trainer.py    # Trainer management tests
├── test_session.py    # Session entity tests
├── test_booking.py    # Booking system tests
├── test_membership.py # Membership rules tests
└── test_schedule.py   # Schedule and conflict tests
```


## Build and Run Instructions


### Prerequisites


- **Python 3.8+** (Recommended: Python 3.9 or higher)
- **Git** (for version control)
- **Terminal/Command Prompt** access


### Installation


1. **Clone or Download the Project**
  ```bash
  # If using git
  git clone <repository-url>
  cd D1
 
  # Or download and extract the project files
  ```


2. **Verify Python Installation**
  ```bash
  python3 --version
  # Should show Python 3.8+
  ```


3. **Set Up Project Structure**
  ```bash
  # Navigate to project directory
  cd /path/to/D1
 
  # Verify structure
  ls -la
  # Should show: src/ tests/ README.md PROJECT_PITCH.md etc.
  ```


### Running the Tests


#### Option 1: Run All Tests (Recommended)
```bash
# From the D1 project root directory
python3 -m unittest discover tests/ -v


# Expected output: 60 tests should pass
# - 25 Client tests
# - 35 Trainer tests
```


#### Option 2: Run Individual Test Files
```bash
# Run only Client tests
python3 -m unittest tests.test_client -v


# Run only Trainer tests 
python3 -m unittest tests.test_trainer -v
```


#### Option 3: Run Specific Test Methods
```bash
# Run a specific test class
python3 -m unittest tests.test_client.TestClient -v


# Run a specific test method
python3 -m unittest tests.test_client.TestClient.test_valid_client_creation_standard_membership -v
```
