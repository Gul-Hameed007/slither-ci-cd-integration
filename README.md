# Slither Analysis Workflow for GitHub Actions

Slither is a Solidity static analysis tool developed by Trail of Bits that identifies vulnerabilities and bugs in Solidity contracts. This repository provides a GitHub Actions workflow to seamlessly integrate Slither's analysis into your CI/CD process.

## Simplified Slither Analysis Configuration

For users and repositories that might not have access to GitHub Advanced Security (required for the SARIF feature), we've simplified the process to still benefit from Slither's analysis. This configuration will run Slither, save the analysis results in a file, commit that file to your repository, and also upload the analysis as an artifact. This ensures that you have easy access to the analysis output both within the repo and as a downloadable artifact.


## 📌 Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Integration Steps](#integration-steps)
- [Workflow Breakdown](#workflow-breakdown)
- [Customizing the Analysis with Printers](#customizing-the-analysis-with-printers)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- **Automated Analysis**: Runs Slither on every push and pull request.
- **Persistent Results**: Saves analysis results as a committed file.
- **Downloadable Artifacts**: Makes the analysis available as a downloadable artifact.
- **Simplified Configuration**: Ideal for users without access to GitHub Advanced Security (SARIF feature).

## 🚀 Prerequisites

- A GitHub repository with Solidity contracts.
- Familiarity with GitHub Actions (for custom modifications, if any).

## 🛠 Integration Steps

1. Navigate to your repository's `.github/workflows/` directory.
2. Create a new YAML file (e.g., `slither-analysis.yml`).
3. Copy and paste the provided workflow script into this YAML file.
4. Commit and push your changes.
5. The workflow will now be activated and run the Slither analysis on every push and pull request.

## 📜 Workflow Breakdown

- **Checkout Repository**: Checks out the latest code.
- **Run Slither Analysis**: Executes Slither targeting the 'Contracts' directory.
- **Save Analysis to File**: Stores the results in `slither-output.txt`.
- **Upload as Artifact**: Provides the Slither output as an artifact named 'slither-report'.

## 🛠 Customizing the Analysis with Printers

Slither offers various "printers" which can generate additional reports, diagrams, or specific information regarding the smart contract. To customize your analysis, you can utilize these printers by adding them to the `slither-args` field in the workflow. For a full list of available printers and their functionalities, refer to the [official Slither documentation](https://github.com/crytic/slither).

## 🔗 Useful Links

- [Official Trail of Bits Slither Action](https://github.com/marketplace/actions/slither-action)

## 🤝 Contributing

We welcome contributions! 

## 📄 License





