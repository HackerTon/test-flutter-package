# IMPORTANT GUIDELINES

## Pending concern to be rectify
* Solve problem with overriding standard function in packages such `constant_util.dart`.
* What is the definition of major, minor, bugfix and buildnumber. When do we increment each category? 

## For every single you need to follow such guidelines
1. Every project must have version name format as given `version: major.minor.bugfix+buildnumber` as start with `0.0.1+1` as the first commit. Pre-production version must be `0.x.x+x`.
2. The standard branching strategy is based on trunking based development. Which consist of only development and production.
    > **NO COMMIT INSIDE OF PRODUCTION OR DEVELOPMENT BRANCH DIRECTLY**.
3. You must move all standard code to packages.


## How to submit changes to development branch
1. Create a branch and name it with ticket id or summarized ticket description.
2. Before merging, make sure to keep your local development branch updated by running `git fetch origin development:development` and then `git merge development`.
3. To merge the branch into development. Run `git checkout development` and `git merge --no-ff --log branch`. *branch is the name of your featurechange.*
4. Delete branch with `git branch -d branch` and `git push --delete origin branch`.

## How to change version
1. Update the version name and commit to development directly.

## How to publish to production
1. Increase minor version and set bugfix version to 0. Example, 1.2.0+1000 from 1.1.48+999.
2. Merge changes to production with `git merge --no-ff --log development`