# git Command line interface
I've created a local Git repository to experiment with different Git commands.


## git flow

it checkout develop
git checkout -b feature_branch

git checkout develop
git merge feature_branch

git checkout develop
git checkout -b release/0.1.0

git checkout master
git merge release/0.1.0

git checkout master
git checkout -b hotfix_branch

git checkout master
git merge hotfix_branch
git checkout develop
git merge hotfix_branch
git branch -D hotfix_branch


## Example

git checkout master
git checkout -b develop
git checkout -b feature_branch

# work happens on feature branch
git checkout develop
git merge feature_branch
git checkout master
git merge develop
git branch -d feature_branch

git checkout master
git checkout -b hotfix_branch


## work is done commits are added to the hotfix_branch
git checkout develop
git merge hotfix_branch
git checkout master
git merge hotfix_branch

1. A develop branch is created from master
2. A release branch is created from develop
3. Feature branches are created from develop
4. When a feature is complete it is merged into the develop branch
5. When the release branch is done it is merged into develop and master
6. If an issue in master is detected a hotfix branch is created from master
7. Once the hotfix is complete it is merged to both develop and master
