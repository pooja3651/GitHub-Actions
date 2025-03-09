# GitHub-Actions

This repository contains workflows for GitHub Actions , which automate tasks like building, testing, and deploying applications.


## 📂 Directory Structure


GitHub-Actions/ │── .github/ │ ├── workflows/ │ │ ├── my-first-actions.yml │── README.md



## 🛠 About `my-first-actions.yml`
The `.github/workflows/my-first-actions.yml` file defines a **simple workflow** that runs when code is pushed to the `main` branch.

### 🔹 Workflow Overview:
- **Triggers on push** to the `main` branch
- **Checks out repository code**
- **Prints "Hello, GitHub Actions!"** in the workflow logs

## 🚀 How to Use
1. **Clone this repository** to your EC2 instance:
   ```bash
   git clone https://github.com/pooja3651/GitHub-Actions.git
   cd GitHub-Actions

## Create/Edit Workflow File:

vim .github/workflows/my-first-actions.yml


#Commit and Push:

git add .
git commit -m "Added my first GitHub Actions workflow"
git push origin main


##📊 Checking Workflow Runs
Go to your GitHub Repository
Click the "Actions" tab
Select the latest run to view log to view logs and results


