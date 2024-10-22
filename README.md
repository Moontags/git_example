# Git Practice Project git_example

This is a practice project to demonstrate various Git functionalities, including branching, merging, stashing, and creating pull requests. The project includes simple text file modifications to showcase Git version control commands.

## Project Overview

The purpose of this project is to learn and practice fundamental Git commands and workflows. By working through this project, the following concepts were explored:

- **Creating a repository**: Initialize a local Git repository.
- **Branching and merging**: Work on different branches and merge changes back into the main branch.
- **Git stash**: Temporarily store uncommitted changes and apply them later.
- **Tags**: Tagging specific commits for versioning.
- **Pull Requests**: Create a pull request for code review and merging.
- **Conflict resolution**: Resolve merge conflicts between branches.

## Key Git Commands Used

- `git init`: Initialize a new Git repository.
- `git add`: Add files to the staging area.
- `git commit`: Commit changes with a message.
- `git checkout -b <branch>`: Create a new branch and switch to it.
- `git merge`: Merge changes from one branch to another.
- `git stash`: Temporarily save changes without committing.
- `git stash pop`: Apply stashed changes and remove them from the stash list.
- `git tag`: Create tags for specific commits.
- `git push`: Push changes to a remote repository.



## Commands

1. **Navigate to the project folder and initialize a Git repository:**
    ```bash
    cd ~/desktop/git_example
    git init
    ```

2. **Create an HTML file and add it to version control:**
    ```bash
    echo "Example" > index.html
    git add index.html
    git commit -m "My example"
    ```

3. **Create a new branch and add a new text file:**
    ```bash
    git checkout -b new_example
    echo "This is a new example" >> example.txt
    git add example.txt
    git commit -m "Added a new example"
    ```

4. **Switch back to the main branch and merge the new branch:**
    ```bash
    git checkout master
    git merge new_example
    ```

5. **Add a remote repository and push changes:**
    ```bash
    git remote add origin https://github.com/Moontags/git_example.git
    git push -u origin master
    ```

6. **Make changes and revert them:**
    ```bash
    echo "This is a change in the example file." >> example.txt
    git add example.txt
    git commit -m "Changes to example.txt"
    git checkout HEAD~1 example.txt
    git add example.txt
    git commit -m "Reverted example.txt to the previous version"
    git push origin master
    ```

7. **Create new branches and add changes:**
    ```bash
    git checkout -b new_test
    echo "This is a new test" >> example.txt
    git add example.txt
    git commit -m "Added new test"
    git push origin new_test
    ```

8. **Create additional branches and add changes:**
    ```bash
    git checkout master
    git checkout -b branch-1
    echo "Change from branch-1" >> example.txt
    git add example.txt
    git commit -m "Changes from branch-1"
    git push origin branch-1

    git checkout master
    git checkout -b branch-2
    echo "Change from branch-2" >> example.txt
    git add example.txt
    git commit -m "Changes from branch-2"
    git push origin branch-2
    ```

9. **Merge branches and resolve any conflicts:**
    ```bash
    git merge branch-1
    git merge branch-2
    open -e example.txt # Resolve conflicts
    git add example.txt
    git commit -m "Resolved merge conflict between branch-1 and branch-2"
    git push origin master
    ```

## Notes
- Make sure to resolve any merge conflicts carefully.
- Don't rush, and you'll avoid unnecessary mistakes.
- Use descriptive commit messages for better understanding of changes.


## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/Moontags/git_example.git
    ```

2. Navigate to the project directory:
    ```bash
    cd git_example
    ```

3. Checkout the main branch or create a new branch:
    ```bash
    git checkout -b <new-branch>
    ```

4. Modify files, commit your changes, and practice Git workflows.

## License

This project is for learning purposes and is open-source.
You are welcome to contribute by adding Git command examples. 
If you have any useful commands or workflows that could benefit others, please feel free to include them in this document. 

