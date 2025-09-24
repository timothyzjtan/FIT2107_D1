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


### Running the Application


#### Interactive Testing (Current Implementation)
```bash
# From the D1 project root directory
python3 -c "
from src.client import Client, MembershipType
from src.trainer import Trainer, TrainerSpecialty
from datetime import time


# Create a sample client
client = Client('C001', 'John Doe', 'john@email.com', MembershipType.STANDARD)
print('Created client:', client)


# Create a sample trainer
trainer = Trainer('T001', 'Jane Smith', 'jane@fitness.com',
                [TrainerSpecialty.YOGA, TrainerSpecialty.PILATES],
                start_time=time(9, 0), end_time=time(17, 0))
print('Created trainer:', trainer)


# Test booking eligibility
print('Can client book?', client.can_book_session())
print('Trainer available at 10 AM?', trainer.is_available_at_time(time(10, 0)))
"
```


#### Future: Main Application (Planned)
```bash
# When main.py is implemented
python3 -m src.main


# Or
python3 src/main.py
```


### Development Workflow


#### Test-Driven Development (TDD)
```bash
# 1. Write a failing test
python3 -m unittest tests.test_new_feature -v


# 2. Implement minimal code to pass
# Edit src/ files


# 3. Run tests to verify
python3 -m unittest discover tests/ -v


# 4. Refactor and repeat
```


#### Adding New Features
```bash
# 1. Create test file
touch tests/test_new_feature.py


# 2. Write comprehensive tests
# Edit tests/test_new_feature.py


# 3. Create implementation file
touch src/new_feature.py


# 4. Implement feature following TDD
# Edit src/new_feature.py


# 5. Run full test suite
python3 -m unittest discover tests/ -v
```


### Troubleshooting


#### Common Issues


1. **ImportError: No module named 'src'**
  ```bash
  # Ensure you're running from the D1 root directory
  pwd  # Should end with /D1
  ls   # Should show src/ and tests/ directories
  ```


2. **Python command not found**
  ```bash
  # Try alternative Python commands
  python --version
  python3 --version
  py --version  # Windows
  ```


3. **Tests failing unexpectedly**
  ```bash
  # Run with more verbose output
  python3 -m unittest discover tests/ -v
 
  # Run individual test to isolate issue
  python3 -m unittest tests.test_client.TestClient.test_specific_method -v
  ```


#### Verification Commands
```bash
# Check project structure
find . -name "*.py" | head -10


# Count test methods
grep -c "def test_" tests/test_client.py tests/test_trainer.py


# Verify all files are present
ls src/
ls tests/
```
rchitecture


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


### Running the Application


#### Interactive Testing (Current Implementation)
```bash
# From the D1 project root directory
python3 -c "
from src.client import Client, MembershipType
from src.trainer import Trainer, TrainerSpecialty
from datetime import time


# Create a sample client
client = Client('C001', 'John Doe', 'john@email.com', MembershipType.STANDARD)
print('Created client:', client)


# Create a sample trainer
trainer = Trainer('T001', 'Jane Smith', 'jane@fitness.com',
                [TrainerSpecialty.YOGA, TrainerSpecialty.PILATES],
                start_time=time(9, 0), end_time=time(17, 0))
print('Created trainer:', trainer)


# Test booking eligibility
print('Can client book?', client.can_book_session())
print('Trainer available at 10 AM?', trainer.is_available_at_time(time(10, 0)))
"
```


#### Future: Main Application (Planned)
```bash
# When main.py is implemented
python3 -m src.main


# Or
python3 src/main.py
```


### Development Workflow


#### Test-Driven Development (TDD)
```bash
# 1. Write a failing test
python3 -m unittest tests.test_new_feature -v


# 2. Implement minimal code to pass
# Edit src/ files


# 3. Run tests to verify
python3 -m unittest discover tests/ -v


# 4. Refactor and repeat
```


#### Adding New Features
```bash
# 1. Create test file
touch tests/test_new_feature.py


# 2. Write comprehensive tests
# Edit tests/test_new_feature.py


# 3. Create implementation file
touch src/new_feature.py


# 4. Implement feature following TDD
# Edit src/new_feature.py


# 5. Run full test suite
python3 -m unittest discover tests/ -v
```


### Troubleshooting


#### Common Issues


1. **ImportError: No module named 'src'**
  ```bash
  # Ensure you're running from the D1 root directory
  pwd  # Should end with /D1
  ls   # Should show src/ and tests/ directories
  ```


2. **Python command not found**
  ```bash
  # Try alternative Python commands
  python --version
  python3 --version
  py --version  # Windows
  ```


3. **Tests failing unexpectedly**
  ```bash
  # Run with more verbose output
  python3 -m unittest discover tests/ -v
 
  # Run individual test to isolate issue
  python3 -m unittest tests.test_client.TestClient.test_specific_method -v
  ```


#### Verification Commands
```bash
# Check project structure
find . -name "*.py" | head -10


# Count test methods
grep -c "def test_" tests/test_client.py tests/test_trainer.py


# Verify all files are present
ls src/
ls tests/
```

