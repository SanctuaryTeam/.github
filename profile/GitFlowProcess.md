Start a New Feature:
Create a new branch from the develop branch. Name it something like "feature/my-feature-name."
Implement your feature and commit your changes to this feature branch.

Merge Feature into Develop:
Once your feature is complete, open a Pull Request (PR) to merge the feature branch into the develop branch.
After code review and testing, merge the PR. This keeps the develop branch up-to-date with all completed features.

Prepare for Release:
When you're ready to release a new version, create a release branch from the develop branch. Name it something like "release/version-x.y.z."

Test and Stabilize:
Perform testing and any necessary bug fixes on the release branch.
Only critical bug fixes should be merged into the release branch at this point.

Merge Release into Master/Main and Develop:
Once the release is stable, merge the release branch into both the master/main and develop branches.
This ensures that your main branch is always in sync with the latest stable release.

Hotfixes:
If a critical bug is discovered in the master/main branch, create a hotfix branch from the master/main branch.
Fix the bug and merge the hotfix back into both master/main and develop branches.
.
.
Master/Main Branch: This branch represents the stable codebase that is ready for deployment. No direct development occurs on this branch.

Develop Branch: This branch is used as a integration branch for ongoing development work. All feature branches and bug fixes are merged into this branch.

Feature Branches: Each new feature or task is developed in its own isolated branch. This keeps the main development branch (develop) clean and makes it easier to manage different features concurrently.

Release Branches: When you're preparing to release a new version of your software, you create a release branch from the develop branch. This allows you to stabilize the code for release while still allowing bug fixes and other necessary adjustments.

Hotfix Branches: If a critical bug is discovered in the master/main branch, you create a hotfix branch from master/main, fix the bug, and merge it back into both master/main and develop.
