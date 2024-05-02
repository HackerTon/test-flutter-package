# IMPORTANT GUIDELINES

## Pending concern to be rectify
* Naming for each feature branch.
* Name for git merge commit message.
* Solve problem with overriding standard function in packages such `constant_util.dart`.
* What is the definition of major, minor, bugfix and buildnumber. When do we increment each category? 

## For every single you need to follow such guidelines
1. Every project must have version name format as given `version: major.minor.bugfix+buildnumber` as start with `0.0.1+1` as the first commit.
2. The standard branching strategy is based on trunking based development. Which consist of only development and production.
    > **NO COMMIT INSIDE OF PRODUCTION BRANCH**.
3. Each new bugfix and featurechange must be done on a separate branch and remove once merge into development branch.
4. Make sure you keep your local development branch update to date by running `git fetch development:development` and then `git merge development`.
5. You must move all standard code to packages.