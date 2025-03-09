#  GitHub Actions Workflows  

This repository contains two **GitHub Actions workflows**:  
1️⃣ A **basic workflow** that prints "Hello, GitHub Actions!"  
2️⃣ A **Python testing workflow** that tests an addition function using `pytest`.  

Both workflows **run on self-hosted runners** but can be switched to **Ubuntu-latest**.  

---

## My First GitHub Action  

This workflow prints **"Hello, GitHub Actions!"** whenever a push is made to the `main` branch.  


## What It Does:
✅ Triggers on: Every push to the main branch.
✅ Runs on: A self-hosted runner (change to ubuntu-latest if needed).
✅ Steps:

Checks out the repository.
Prints a message: "Hello, GitHub Actions!"

### My Second GitHub Action (Python Testing Workflow)

This workflow is designed to test a Python function (addition.py) using pytest.

### **What It Does:**
✅ Triggers on: Every push to the repository.
✅ Runs on: A self-hosted runner (can switch to ubuntu-latest).
✅ Matrix Strategy: Runs Python 3.9.
✅ Steps:

Checks out the repository.
Installs Python dependencies.
Runs pytest on test_addition.py in the src/ folder.

### Repository Structure
```
GitHub-Actions/
│-- .github/
│   └── workflows/
│       ├── my-first-action.yml  # Prints "Hello, GitHub Actions!"
│       ├── my-second-action.yml # Runs Python tests
│-- src/
│   ├── addition.py              # Python script for addition
│   ├── test_addition.py         # Unit test for addition.py
│-- README.md                    # This file
```

### Python Code for Testing
src/addition.py (Addition Function)
```py
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
    assert add(-1, 1) == 0
```

### Switching Between Self-Hosted & Ubuntu-Latest
By default, both workflows run on self-hosted runners.
To switch to Ubuntu-latest, modify the runs-on parameter:

runs-on: ubuntu-latest


### How to Use This Repo?
1️⃣ Clone the Repository:

git clone https://github.com/pooja3651/GitHub-Actions.git
cd GitHub-Actions

Push Changes to Trigger Actions:

```sh
git add .
git commit -m "Trigger GitHub Actions"
git push origin main 
```

## Conclusion
This repository demonstrates two GitHub Actions workflows:

A basic workflow printing a message.
A Python testing workflow using pytest.
Both workflows run on self-hosted runners but can be switched to ubuntu-latest if needed.

