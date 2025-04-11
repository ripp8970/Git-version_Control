### Task 1: Initialize Local Repository and Push to GitHub

1.  **Create a new project directory:**
    ```bash
    mkdir my-devops-project
    cd my-devops-project
    ```

2.  **Initialize a Git repository:**
    ```bash
    git init
    ```

3.  **Create an initial file (e.g., `initial.txt`):**
    ```bash
    echo "Initial commit" > initial.txt
    ```

4.  **Stage the file:**
    ```bash
    git add initial.txt
    ```

5.  **Create the initial commit:**
    ```bash
    git commit -m "Initial commit"
    ```

6.  **Create a new repository on GitHub:**
    * Go to [https://github.com/new](https://github.com/new).
    * Give your repository a name (e.g., `my-devops-project`).
    * You can choose to make it public or private.
    * Do **not** initialize it with a README, license, or `.gitignore` on GitHub, as we are doing this locally.
    * Click "Create repository".

7.  **Link the local repository to the remote GitHub repository:**
    * Copy the HTTPS or SSH URL of your newly created repository from GitHub.
    * Run the following command in your local repository (replace `<YOUR_GITHUB_URL>` with the copied URL):
      ```bash
      git remote add origin <YOUR_GITHUB_URL>
      ```
8.  **Push the local `master` branch to the remote `origin` repository:**
    ```bash
    git push -u origin master
    ```

### Task 2: Create Development and Feature Branches

1.  **Create the `dev` branch from `master`:**
    ```bash
    git checkout -b dev master
    ```

2.  **Switch back to the `master` branch:**
    ```bash
    git checkout master
    ```

3.  **Create a `feature` branch (e.g., `feature-pipeline`) from `dev`:**
    ```bash
    git checkout -b feature-pipeline dev
    ```

4.  **Push the `dev` and `feature-pipeline` branches to GitHub:**
    ```bash
    git push origin dev
    git push origin feature-pipeline
    ```

### Task 3: Use Pull Requests for Merging

1.  **Make changes on the `feature-pipeline` branch:**
    * Create a new file `pipeline.sh` with some basic content:
        ```bash
        echo "#!/bin/bash" > pipeline.sh
        echo "echo 'Running the pipeline...'" >> pipeline.sh
        chmod +x pipeline.sh
        ```
    * Stage and commit the changes:
        ```bash
        git add pipeline.sh
        git commit -m "Add basic pipeline script"
        ```

2.  **Push the changes on the `feature-pipeline` branch to GitHub:**
    ```bash
    git push origin feature-pipeline
    ```

3.  **Create a Pull Request on GitHub:**
    * Go to your repository on GitHub.
    * You should see a notification about your recently pushed `feature-pipeline` branch. Click "Compare & pull request".
    * Alternatively, go to the "Pull requests" tab and click "New pull request".
    * Select the `base` branch as `dev` and the `compare` branch as `feature-pipeline`.
    * Add a descriptive title and a comment explaining the changes in the pull request.
    * Click "Create pull request".

4.  **Review and Merge the Pull Request:**
    * Click the "Merge pull request" button.
    * Confirm the merge.
    * You can then choose to delete the `feature-pipeline` branch on GitHub.

5.  **Update your local `dev` branch:**
    ```bash
    git checkout dev
    git pull origin dev
    ```

6.  **Now, let's merge the `dev` branch into the `master` branch using another Pull Request:**
    * Make some changes on the `dev` branch (e.g., edit `initial.txt`):
        ```bash
        echo "Updated initial file in dev" >> initial.txt
        git add initial.txt
        git commit -m "Update initial file in dev"
        git push origin dev
        ```
    * Create a new Pull Request on GitHub with `base` as `master` and `compare` as `dev`.
    * Add a title and description, and click "Create pull request".
    * Review and merge the pull request.
    * (Optional) Delete the `dev` branch on GitHub.

7.  **Update your local `master` branch:**
    ```bash
    git checkout master
    git pull origin master
    ```

### Task 4: Adding readme file(README.md)

* Created `README.md` with project information.
* Staged, committed, and pushed the file.
* Run the following commands:
  ```bash
  git add README.md
  git commit -m "Add comprehensive README.md"
  git push origin master
  ```

### Task 5: Create a gitignore file(.gitignore)
* Created `.gitignore` with common DevOps exclusions(Adapt the .gitignore file based on your actual project needs. Stage and commit the .gitignore file).
* Staged, committed, and pushed the file by running the following commands.
    ```bash
    git add .gitignore
    git commit -m "Add .gitignore for common DevOps project files"
    git push origin master
    ```
### Task 6: Use Git Tags

1.  **Switch to the `master` branch:**
    ```bash
    git checkout master
    ```

2.  **Create an annotated tag for a release (e.g., `v1.0.0`):**
    ```bash
    git tag -a v1.0.0 -m "Initial stable release"
    ```

3.  **List the tags:**
    ```bash
    git tag
    ```

4.  **Show information about a specific tag:**
    ```bash
    git show v1.0.0
    ```

5.  **Push the tag(s) to the remote repository:**
    ```bash
    git push origin --tags
    ```

6.  **(Optional) Create a lightweight tag:**
    ```bash
    git tag v1.0
    git push origin v1.0
    ```
### Task 7: Adding tasks file(TASKS.md)
* Staged, committed, and pushed the file by running the following commands.
  ```bash
  git add TASKS.md
  git commit -m "Document all tasks in TASKS.md"
  git push origin main
  ```