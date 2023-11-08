# Feature Journey Workflow :rocket:

This document outlines the workflow for handling features from their inception to deployment.

## Workflow Steps :hammer_and_wrench:

1. **Issue Assignment :white_check_mark::** Developers pick up Jira issues assigned to them.

2. **Feature Branch Creation :herb::**

   - Developers spawn new feature branches tied to specific issues for feature implementation.

   - A new feature branch is derived from the `develop` branch using the branch naming convention `feature/feature-name` or `feature/ticket-number`.

     ```git
     git checkout -b feature/feature-name develop
     ```

     **Visualizing the Branching Journey**
     The visual representation of this branching strategy takes shape like this:

     ```
     feature/feature-name      ---o-----o
                             /
     develop ---------------o

     ```

3. **Local Testing :test_tube: :**

   - Developers finalize feature development and conduct comprehensive local tests.
   - Developers has also wrapped up composing the requisite test cases.

4. **Pull Request (PR) to Develop :rocket::**

   - A pull request (PR) is initiated, targeting the `develop` branch, featuring an informative commit summary.
   - The PR includes a detailed commit message summarizing the changes made.
   - The PR assignment engages reviewers for assessment.

5. **PR Review and Feedback :speech_balloon::**

   - Reviewers scrutinize code modifications and furnish constructive feedback.
   - Developers respond by effecting necessary revisions and updates.

6. **PR Approval and Merge to Develop :white_check_mark::**

   - Once the code is reviewed and approved, it is merged into the `develop` branch. The PR should be reviewed by at least two other team members.
   - The `feature/feature-name` branch will be deleted from the origin after the merge.
   - Continuous Integration (CI)/ Continous Deployment (CD) processes are triggered for automated testing and deployment.
   - The updated code is deployed to the Dev Environment. Access the deployed feature via [Dev Environment URL](https://dev-portal.zoopsign.com/).

7. **Develop to Staging :flight_departure::**

   - When you're nearing a release date and develop has all the desired features, create a release branch like `release/v<latest_version>`. This branch is for:

     - Bug fixes related to the release.
     - Preparing release notes.
     - Final integration testing.

     ```git
     git checkout -b release/vX.Y.Z develop
     ```

     **Visualizing the Branching Journey**
     The visual representation of this branching strategy takes shape like this:

     ```
     release/vX.Y.Z     ----o-----o
                       /
     develop ---------o
     ```

   - Periodically, after QA testing and when a set of features are ready, the `release/vX.Y.Z` branch is merged into the `staging` branch.
   - The updated code is deployed to the Staging Environment. Access the deployed features via [Staging Environment URL](https://staging-portal.zoopsign.com/).
   - Further testing and integration take place in the staging environment.
   - Any bug fixes related to the release are done in this branch.

8. **Staging to Main (Production) :ship::**

   - After successful staging and final approval, the `release/vX.Y.Z` branch is merged into the `main` branch (production) and also in the `develop` branch (development).
   - The feature is now deployed and live.

9. **Support for Feature (Bug Fixes) :ship::**

   - In case of critical bugs in the `main` branch, a branch is created from `main` for quick fixes, e.g., `hotfix/bug-description`.
   - Once fixed, it will deploy on staging and tested.
   - Once tested the feature branch will be marked as `release/v<latest_version>`.
   - It is merged back into both `master/main` and `develop`.
     ```
     git checkout -b hotfix/fix-description master
     ```
     **Visualizing the Branching Journey**
     The visual representation of this branching strategy takes shape like this:
     ```
     hotfix/fix-description    ---o
                             /
     master -----------------o
     ```

**Note**: For more branching details, please refer to the following link: [Git Branching Guidelines](https://zoop.atlassian.net/l/cp/HvWXr64w).

## Conclusion :tada:

This workflow ensures a systematic and controlled process for introducing new features, from development and testing to deployment in production.
