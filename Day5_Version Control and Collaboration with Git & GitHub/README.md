# Web Genesis: Day 5 - Version Control and Collaboration with Git & GitHub

**Welcome back to Web Genesis!** Today we delve into the essential tools for collaborative software development: Git and GitHub.

**1. Git: The Foundation of Version Control**

* **What is Git?** 
    * Git is a powerful version control system that allows you to track changes to your code over time. 
    * It enables you to:
        * **Revert to previous versions:** Easily go back to earlier versions of your code if needed.
        * **Experiment freely:** Create branches to try out new ideas without affecting the main codebase.
        * **Collaborate effectively:** Work with others on the same project seamlessly.

* **Core Git Concepts:**
    * **Repository:** A directory that contains all the files for your project and the Git history of those files.
    * **Commit:** A snapshot of your code at a particular point in time. Each commit has a unique identifier and a message describing the changes made.
    * **Branch:** A separate line of development. You can create branches to work on new features, experiment with ideas, or fix bugs without affecting the main codebase.
    * **Staging Area:** A temporary area where you prepare changes to be committed. You can selectively stage changes before committing them.

* **Essential Git Commands:**
    * `git init`: Initializes a new Git repository in your current directory.
    * `git clone`: Creates a local copy of an existing Git repository from a remote server (like GitHub).
    * `git add`: Stages changes to files in the staging area, preparing them for the next commit.
    * `git commit`: Creates a new commit with the staged changes.
    * `git status`: Shows the current state of your working directory, including any unstaged changes.
    * `git log`: Displays the history of commits in your repository.
    * `git diff`: Shows the differences between the current state of your files and the previous commit.

* **Git Workflows:**
    * Learn common Git workflows, such as the Gitflow workflow, which provides a structured approach to branching and merging for managing releases and features.

**2. Collaborating with GitHub**

* **GitHub Basics:**
    * Create a GitHub account and familiarize yourself with the GitHub interface.
    * Learn how to create and manage repositories on GitHub, including setting permissions and collaborating with others.

* **Pull Requests:**
    * Learn how to create and review pull requests, the cornerstone of collaborative development on GitHub.
    * **Creating a Pull Request:**
        * Create a new branch for your feature or bug fix.
        * Make your changes and commit them to your branch.
        * Create a pull request on GitHub, describing the changes you made and requesting that your changes be merged into the main branch.
    * **Reviewing Pull Requests:**
        * Provide constructive feedback on the code, suggest improvements, and ensure code quality.
        * Approve or request changes to pull requests.

* **Branching and Merging:**
    * Understand the importance of branching for parallel development and how to effectively merge branches.
    * Learn how to create and manage branches for different features, bug fixes, and experiments.
    * Understand how to resolve merge conflicts that may arise when merging branches.

**Mini-Project: Host your React App on GitHub Pages**

Today's challenge: Host your React application on GitHub Pages.

* **Steps:**
    * Create a new branch in your GitHub repository specifically for GitHub Pages deployment (e.g., `gh-pages`).
    * Build your React application for production (usually by running `npm run build` or `yarn build`).
    * Configure your GitHub Pages settings to serve your built application from the `gh-pages` branch.
    * Customize the GitHub Pages settings to match your desired domain or project URL.

**Resources:**

* **GitHub Help:** [https://docs.github.com/](https://docs.github.com/) - Extensive documentation on all things GitHub.
* **Git - The Simple Guide:** [https://learngitbranching.js.org/](https://learngitbranching.js.org/) - Interactive guide to learning Git branching.
* **Pro Git Book:** [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2) - A comprehensive guide to Git.

**Let's get coding!**

This enhanced README provides a comprehensive guide for Day 5 of Web Genesis, covering essential Git and GitHub concepts with detailed explanations and practical examples. Remember to practice these concepts and explore the vast resources available to deepen your understanding of version control and collaboration.

**Bonus Tip:** Explore GitHub Actions to automate your workflows, such as building, testing, and deploying your applications directly from GitHub.


## *Created by:*

*Atharva Wakodikar*

---

## *Contributing*

Feel free to contribute by suggesting edits, adding more resources, or sharing your learning experiences.