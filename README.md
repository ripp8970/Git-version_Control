# Git-Version_Control Project

This project serves as a demonstration of Git best practices for managing a DevOps workflow. It includes basic configuration files and scripts that might be part of a typical DevOps setup.

## Project Structure

.

├── .gitignore

├── README.md

├── TASKS.md

├── initial.txt

└── pipeline.sh

## Branches

* **`master`:** The stable, production-ready branch. All releases are tagged here.
* **`dev`:** The master development branch where ongoing work is integrated.
* **`feature-*`:** Feature-specific branches branched from `dev` for implementing new functionalities or bug fixes.

## Workflow

1.  New features or bug fixes are developed in dedicated `feature` branches, branched off from `dev`.
2.  Once a feature is complete, a Pull Request is created to merge the `feature` branch into `dev`.
3.  Code reviews are performed on the Pull Request.
4.  Upon successful review, the Pull Request is merged into `dev`.
5.  Periodically, when a set of features is ready for release, a Pull Request is created to merge `dev` into `master`.
6.  The `master` branch is tagged with a release version number.

## Getting Started

1.  Clone the repository:
    ```bash
    git clone https://github.com/ripp8970/Git-version_control.git
    cd Git-version_control
    ```
2. Perform the given commands in # TASKS.md https://github.com/ripp8970/Git-version_control/blob/master/TASKS.md