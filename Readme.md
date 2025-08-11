## Git Version Control for DevOps Project
This project demonstrates how to manage a DevOps project using Git best practices, incorporating proper commits, branching strategies, pull requests, and repository configuration.

## Objective
-  Use Git to manage code changes and project versions.
- Implement a branching strategy with `main`, `dev`, and `feature` branches.
- Use pull requests for code review and merging.
- Maintain a clean commit history with meaningful commit messages.
- Utilize `.gitignore` to exclude unnecessary files.
- Tag releases for versioning.

## Tools Used
- **Git**: Distributed version control system.
- **GitHub**: Hosting service for Git repositories.

## Project Structure & Workflow

### Branching Strategy
- `main` - Production-ready stable code.
- `dev` - Integration branch for development.
- `feature/*` - Branches created off `dev` for specific features or tasks.

### Commit Guidelines
- Make small, atomic commits with clear messages.
- Follow commit message best practices.

## Pull Request Workflow
1. **feature → dev**
* Feature branch changes are reviewed and merged into dev
2. **dev → main**
* Tested and stable changes are merged into main
3. **Tag Release**
* Tag created after merge to main for version tracking

## Step-by-Step Guide: Version-Controlled DevOps Project with Git

1. **Initialize the Git Repository**
* Open your terminal and navigate to your project folder.
* Initialize Git:
```
git init
```
2. **Create Repository on GitHub and Add Remot**e
* Go to GitHub and create a new repository (e.g., DevOps-test-day4).

* Add the remote URL to your local repo:
```
git remote add origin <your-repo-URL>
git branch -M main
git push -u origin main
```
3. **Establish Branching Strategy**
*  Create a development branch:
```
git checkout -b dev
git push -u origin dev
```
* Create a feature branch for isolated development:
```
git checkout -b feature/add-ci-cd
git push -u origin feature/add-ci-cd
```
4. **Create a .gitignore File**
* Create a .gitignore file to exclude files/folders that shouldn't be tracked:
```
echo 'node_modules/' >> .gitignore
git add .gitignore
git commit -m "Add .gitignore"
git push
```
( Add other entries as needed )
5. **Add a Build Script (Optional)**
* Create a sample build script:
```
echo "echo 'Running build...'" > build.sh
chmod +x build.sh
git add build.sh
git commit -m "Add basic build script"
git push
```
6. **Commit Regularly with Meaningful Messages**
* Make changes and commit them frequently with clear messages describing each change.
7. **Pull Request (PR) Workflow**
* From ```feature``` to ```dev```:
* Push your feature branch to GitHub.

* Open a Pull Request from ```feature/add-ci-cd``` → ```dev```.

* Review and merge after approvals.

* From dev to main:
* When changes are stable and tested, open a Pull Request from ```dev``` →```main```.

* Review and merge after testing.

8. **Tag Releases**
* After your changes are merged to main, create a version tag to mark releases:
```
git tag -a v1.0 -m "First stable release"
git push origin v1.0
```
9. **Write Proper Documentation**
* Edit or create a README.md file explaining your project's purpose, setup, and workflow.

* Add additional markdown files like docs.md for detailed steps and documentation.

* Track all documentation in the repository.

10. **Summary of Best Practices**
- Use branches for features and development.

- Submit and review pull requests for merging.

- Tag stable releases for versioning.

- Keep repository documentation current.

By following these steps, you'll have a robust, version-controlled DevOps project that follows industry standards for collaboration and traceability.

## Commands Used 
```
# Initialize repository
git init

# Add remote and push to GitHub
git remote add origin <repo-URL>
git branch -M main
git push -u origin main

# Create branches
git checkout -b dev
git push -u origin dev
git checkout -b feature/add-ci-cd
git push -u origin feature/add-ci-cd

# Add build script
echo "echo 'Running build...'" > build.sh
chmod +x build.sh
git add build.sh
git commit -m "Added basic build script"
git push

# Create and push tag
git tag -a v1.0 -m "First stable release"
git push origin v1.0
```