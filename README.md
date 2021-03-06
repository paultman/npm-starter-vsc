# Basic NPM based starter project

This code is part of a guide to setup a Visual Studio Code javascript project with uses Eslint, the Airbnb Style Guide, Stylelint and Prettier.

It is meant to support a VSC project using the EsLint and Prettier extensions.

All configuration is local to the project itself.
See the blogpost at https://paultman.com/setup-visual-studio-code-on-an-m1-mba-in-2021/

Feel free to use this as a project starter and update it for your own project by:

- Cloning the repo into your own project directory
  ie: git clone https://github.com/paultman/npm-starter-vcs.git my-own-project
- CD into your repo and remove my initial git repo by running: rm -rf .git
- Initialize your own git repo: git init .
- Update the readme.md and package.json files to reflect your information and unique project.
- Add all files to your local repo: git add .
- Do your first commit to your newly created repo: git comit -m "initial comit for my own project"

### Update March 31, 2022

I am working on another projected and noticed that this starter is a bit outdated. I'll update it now and in the future, after cloning check if it's out of date:

- npm list //show currently installed packages
- npm outdated //show outdated packages
- npm update //update packages up to semver in package.json

If you are starting a new project, best to update packages and commit before getting started with your own code.

#### Reference

Check out the npm page for semantic versioning and how it is used.

https://docs.npmjs.com/about-semantic-versioning

In a nutshell:

[majorBreakingVersion].[backward compatible feature add].[bugfix]

So when starting a project, you want to get the latest version available. Afterwards, when making updates, you'll use ~ to signify allowing bug change updates the the package, and ^ to signify allowing new feature updates to a package.

For Example:

eslint: ^8.12.0 which means to allow any future package updates like 8.13.0 or even 8.13.1

If instead you used: ~8.12.0, you would only update with bugfixes, for example to 8.12.1.

If you don't use either prefix (~ or ^) then you only want the exact version specified, no future auto-upgrades.
