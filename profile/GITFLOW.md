Git Workflow
1. Start a New Feature

    Action: Create a new branch from the develop branch.
    Naming: Format it like feature/my-feature-name.
    Task: Implement your feature and commit your changes to this feature branch.

2. Merge Feature into Develop

    Action: Open a Pull Request (PR) to merge the feature branch into the develop branch.
    Process: After code review and testing, merge the PR.
    Benefit: Keeps the develop branch up-to-date with all completed features.

3. Prepare for Release

    Action: Create a release branch from the develop branch.
    Naming: Format it like release/version-x.y.z.

4. Test and Stabilize

    Action: Perform testing and any necessary bug fixes on the release branch.
    Note: Only critical bug fixes should be merged into the release branch at this point.

5. Merge Release into Main and Develop

    Action: Merge the stable release branch into both the main and develop branches.
    Benefit: Ensures the main branch is always in sync with the latest stable release.

6. Hotfixes

    Issue: If a critical bug is discovered in the main branch.
    Action: Create a hotfix branch from the main branch, fix the bug, and merge the hotfix back into both main and develop branches.

Branch Descriptions

    Main Branch: Represents the stable codebase that is ready for deployment. Direct development should not occur on this branch.
    
    Develop Branch: Serves as an integration branch for ongoing development work. All feature branches and bug fixes are merged into this branch.
    
    Feature Branches: Dedicated branch for each new feature or task. Keeps the develop branch clean and facilitates concurrent feature development.
    
    Release Branches: Branches created from the develop branch when preparing for a new version release. Allows code stabilization, bug fixes, and necessary adjustments.
    
    Hotfix Branches: Branches created from master/main when a critical bug is found. They ensure prompt fixes without disrupting the main or develop branches.

