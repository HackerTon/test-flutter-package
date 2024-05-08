# IMPORTANT GUIDELINES

## Pending concern to be rectify

## For every single you need to follow such guidelines
1. Every project must have version name format as given `version: major.minor.bugfix+buildnumber` as start with `0.0.1+1` as the first commit. Pre-production version must be `0.x.x+x`.
2. The standard branching strategy is based on trunking based development. There exist only one main branch and it can be named as trunk/main. Any commit cannot directly committed to main branch except for version update.
[Trunk based development](https://trunkbaseddevelopment.com/).
3. Release is done by tagging.


## How to submit changes to development branch
1. Create a branch and name it with ticket id or summarized description.
2. Before merging, make sure to keep your local trunk branch updated by running `git fetch origin main:main` and then `git merge main`.
3. To merge the branch into trunk. Run `git checkout main` and `git merge --no-ff --log branch`. *branch is the name of your featurechange.*
4. Delete branch with `git branch -d branch` and `git push --delete origin branch`.

## How to change version
1. Update the version name and commit to trunk directly by incrementing bugfix and buildnumber.

## How to do production release
1. Increase minor version and set bugfix version to 0. Example, 1.2.0+1000 from 1.1.48+999.
2. Tag the version update commit with `git tag x.x.0+x`.
3. Build a release version.