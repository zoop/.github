# Contributing to Raftel :rocket:

Welcome to the Raftel repository! We're thrilled that you're considering contributing. This guide will help you navigate the process and make meaningful contributions to the project.

## Getting Started :hammer_and_wrench:

1. **Clone the Repo**: Begin by cloning the repository to your local machine using this command:

   ```bash
   git clone git@bitbucket.org:zoopkyc/zoopsign-frontend.git
   cd zoopsign-nodejs-service
   ```

2. **Install Dependencies**: Next, install the necessary project dependencies using Yarn:

   ```bash
   yarn install
   ```

## Making Changes :hammer_and_wrench:

1. **Create a New Branch**: Start by creating a new branch for your feature or bug fix. Use a descriptive branch name like `feature/<issue_number>-your-feature-name` or `fix/<issue_number>-issue-description`.

   ```bash
   git checkout -b feature/<issue_number>-your-feature-name
   ```

2. **Make Your Changes**: Craft your code while adhering to the project's coding standards and guidelines. Keep your changes focused and well-tested.

3. **Commit Your Changes**: Commit your work with a clear and concise message following the Conventional Commits format. Here are a few commit type examples:

   - `feat`: Add a new feature.
   - `fix`: Fix a bug.
   - `chore`: Routine tasks and maintenance.
   - `docs`: Documentation updates.
   - `style`: Code style adjustments.
   - `refactor`: Code refactoring.
   - `perf`: Performance enhancements.

   Detailed Commit Message Format:

   ```bash
   <type>(<scope>): <description>

   [optional body]

   [optional footer]

   ```

   Example:

   ```bash
   git commit -m "feat(user): add password reset functionality"
   ```

   ```bash
   feat(user): add password reset functionality

   This commit adds the functionality for users to reset their passwords.
   Closes #123

   ---

   fix(auth): resolve authentication token issue

   Fixes an issue where authentication tokens were not being properly generated.

   ```

4. **Push Your Changes**: Push your changes to your forked repository.

   ```bash
   git push origin feature/<task_id>-your-feature-name
   ```

## Submitting Pull Requests 🔁

1. **Open a Pull Request (PR)**: Head over to the original repository and click the "Compare & pull request" button for your branch. Provide a descriptive title and a detailed description of your changes.

2. **Keep Your PR Up-to-date**: If the original repository's `main` branch has new changes, update your branch before your PR is reviewed.

   ```bash
   git fetch upstream
   git checkout main
   git pull upstream main
   git checkout feature/<task_id>-your-feature-name
   git merge main
   ```

3. **Review and Merge**: Expect project maintainers to review your code. Address feedback and make necessary changes. Once approved, your work will merge into the main project.

## Code Style and Guidelines :art:

- Stick to the current code style and formatting.
- Use descriptive and meaningful names for variables and functions.
- Document your code, especially if it involves complex logic.

For more information on the code style and standard checkout our [Style Guide](/docs/STYLE_GUIDE.md)

## Feature Journey

If you're planning to contribute to the project, understanding the feature journey is crucial. Check out our [Feature Journey Documentation](/docs/FEATURE_JOURNEY.md) to familiarize yourself with the development process.

## Reporting Issues :lady_beetle:

If you encounter bugs, issues, or have suggestions, don't hesitate to open an issue on our [issue tracker](https://zoop.atlassian.net/jira/software/projects/ZSAAS/boards/27).

Your contributions are invaluable, and they're helping to make Raftel even more awesome! Thank you!
